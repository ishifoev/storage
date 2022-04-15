## Node JS app for writing data in memory or disk

It is mini app for writing and reading data from memory and disk. Sometimes we just save data and forget it to save it in disk, or may be database crash and all information keep up in one server.

### Usage

* Node.JS version 14 and up 

You need to run inside the terminal
```
node server.js
```

We can do run in another terminal like a client inside the folder to save data in memory

```
curl localhost:3001/memory/foo --header 'Content-Type: application/json' --data '{"data": "This is some data on a memory"}'
```

We can check if this data save in memory

```
curl localhost:3001/memory/foo -w "\n"
```

See how to save in disk data it will the same thing but it will save in your filesystem.

```
curl localhost:3001/disk/foo --header 'Content-Type: application/json' --data '{"data": "This is some data on a disk"}'
```

Check stil you can see it can be see

```
curl localhost:3001/disk/foo -w "\n"
```

For real checking you can reload your server and see if it save when your crash your server and do curl get for both memory and disk.