# MockRedis: A Simple Redis Mock Implementation

MockRedis is a fun project aimed at creating a simple mock implementation of Redis, focusing on key-value pair storage and retrieval using TCP connections. This project aims to provide a basic understanding of how Redis works under the hood and how its commands are processed.

## Getting Started

To get started with MockRedis, follow these steps:

1. Clone the repository to your local machine:

   ```bash
   git clone <repository_url>
   ```

2. Install the necessary dependencies:

   ```bash
   npm install
   ```

3. Start the MockRedis server:

   ```bash
   npm start
   ```

## Connecting To Mock Redis

You can connect to MockRedis using any TCP client, such as telnet or netcat. By default, MockRedis listens on port 8000.

Though In order to utilize it you will be needing the **Redis-cli** you can download it's docker image from [here](https://redis.io/docs/latest/operate/oss_and_stack/install/install-stack/docker/)

## Available Commands

MockRedis supports two basic commands: SET and GET.

## SET Command

The `SET` command is used to set a key-value pair in the database.

**Syntax:**

```bash
SET <key> <value>
```

**Example:**

```bash
SET mykey hello
```

## GET Command

The GET command is used to retrieve the value associated with a key from the database.

**Syntax:**

```bash
GET <key>
```

**Example:**

```bash
GET mykey
```

## Data Storage

MockRedis stores key-value pairs in memory using a simple JavaScript object. Keys and values can be of any type supported by JavaScript.

## Protocol

MockRedis follows a simple serialization protocol for communication over TCP connections. Strings are prefixed with `+` and end with `CRLF (\r\n)`. Errors are prefixed with `-`.

**Example of setting a string value:**

```bash
+OK\r\n
```

**Example of retrieving a string value:**

```bash
$5\r\nhello\r\n
```

## Contributing

Contributions to MockRedis are welcome! Feel free to submit pull requests or open issues for any bugs, feature requests, or suggestions.
