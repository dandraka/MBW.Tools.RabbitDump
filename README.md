# MBW.Tools.RabbitDump

A `dotnet tool` to import / export from RabbitMQ queues

### Features

* Define source and destinations and move messages between them

### Packages

| Package | Nuget |
| ------------- |:-------------:|
| MBW.Tools.RabbitDump | [![NuGet](https://img.shields.io/nuget/v/MBW.Tools.RabbitDump.svg)](https://www.nuget.org/packages/MBW.Tools.RabbitDump) |

### Usage

To install, run: `dotnet tool install --global MBW.Tools.RabbitDump`

To export:
```
rabbitdump --input amqp://myuser:mypass@server:port/vhost --output data.zip queue1 queue2
```

To import:
```
rabbitdump --input data.zip --output amqp://myuser:mypass@server:port/vhost
```

### Todo

* Replay messages with same delays as when they were first created
* RabbitMQ API support to list queues, support wildcards in queue names
* Add AWS SQS queues