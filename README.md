# Useful Linux Commands for CKAD Exam

## General Navigation and File Operations

### ls: List directory contents.
```
$ ls -l
total 4
drwxr-xr-x 2 user user 4096 Jan  1 12:34 directory
-rw-r--r-- 1 user user    0 Jan  1 12:34 file.txt
```

### cd: Change the current directory.
No output for this command, but it changes the current working directory.

### pwd: Print the working directory.
```
$ pwd
/home/user
```

### mkdir: Create a directory.
No output, but creates a new directory.

### rmdir: Remove an empty directory.
No output, but removes an empty directory.

### rm: Remove files or directories.
No output, but the specified files/directories are removed.

### cp: Copy files or directories.
No output, but the files/directories are copied.

### mv: Move or rename files or directories.
No output, but the file/directory is moved or renamed.

### touch: Create an empty file or update the file's timestamp.
No output, but the file is created or updated.

### cat: Concatenate and display files.
```
$ cat file.txt
Hello, World!
```

## Text Manipulation

### echo: Display a line of text.
```
$ echo "Hello World"
Hello World
```

### cut: Remove sections from each line of files.
```
$ echo "name,age" | cut -d',' -f1
name
```

### sort: Sort lines of text files.
```
$ echo -e "c\nb\na" | sort
a
b
c
```

### uniq: Report or omit repeated lines.
```
$ echo -e "a\na\nb" | uniq
a
b
```

### awk: Pattern scanning and processing language.
```
$ echo "field1 field2" | awk '{print $2}'
field2
```

### sed: Stream editor for filtering and transforming text.
```
$ echo "hello" | sed 's/hello/world/'
world
```

## Process Management

### ps: Report a snapshot of the current processes.
Output varies based on running processes.

### top: Display Linux processes in real-time.
Interactive output showing process statistics.

### kill: Send a signal to a process.
No output, but sends the specified signal to the process.

### nohup: Run a command immune to hangups.
```
$ nohup command &
```
Output is redirected to nohup.out.

### bg: Put jobs in background.
No specific output, but moves the job to the background.

### fg: Bring jobs to foreground.
No specific output, but moves the job to the foreground.

## Network Operations

### curl, wget: Download files from the internet.
Output varies, shows download progress and completion.

### ping: Check the network connection to a server.
```
$ ping example.com
PING example.com (93.184.216.34) 56(84) bytes of data.
64 bytes from 93.184.216.34: icmp_seq=1 ttl=56 time=11.632 ms
```

### netstat: Display network connections, routing tables, etc.
Output varies, shows active connections and listening ports.

### nslookup, dig: Query DNS lookup information.
```
$ nslookup example.com
Server:		192.168.1.1
Address:	192.168.1.1#53

Non-authoritative answer:
Name:	example.com
Address: 93.184.216.34
```

## Permissions and Ownership

### chmod: Change file mode bits.
No output, but changes the permissions of the specified file.

### chown: Change file owner and group.
No output, but changes the owner and group of the specified file.

This guide provides a quick overview and examples of common Linux commands along with their expected outputs, useful for CKAD exam preparation.
