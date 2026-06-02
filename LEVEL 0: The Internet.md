# 🌐 How the Internet Works

Before learning APIs, it is important to understand what happens behind the scenes when we open a website.

Let's take a simple example:

```text
google.com
```

When you type `google.com` in your browser and press Enter, many things happen within milliseconds.

---

# Step 1: Browser

A browser is a software application used to access websites.

Examples:

* Google Chrome
* Microsoft Edge
* Firefox
* Safari

When you enter:

```text
google.com
```

the browser starts the process of finding Google's server and requesting the webpage.

```text
User
  ↓
Browser
```

---

# Step 2: DNS (Domain Name System)

Humans remember names like:

```text
google.com
youtube.com
github.com
```

But computers communicate using IP addresses.

The browser asks a DNS server:

> "What is the IP address of google.com?"

Example:

```text
google.com
       ↓
142.250.183.14
```

Think of DNS as the internet's phonebook.

```text
google.com
     ↓
DNS
     ↓
142.250.183.14
```

---

# Step 3: IP Address

An IP address uniquely identifies a device on a network.

Example:

```text
142.250.183.14
```

Just as every house has an address, every server on the internet has an IP address.

Without an IP address, the browser would not know where to send the request.

```text
Browser
   ↓
IP Address Found
```

---

# Step 4: TCP Connection

Before sending data, the browser creates a reliable connection with the server using TCP (Transmission Control Protocol).

TCP performs a process called the Three-Way Handshake.

```text
Browser          Server

SYN      ─────►

         ◄───── SYN-ACK

ACK      ─────►
```

After the handshake, both systems are ready to exchange data.

Think of it like a phone call:

```text
You: Hello?
Server: Hello!
You: Great, let's talk.
```

Now communication can begin.

---

# Step 5: HTTP Request

After the TCP connection is established, the browser sends an HTTP request.

Example:

```http
GET /
Host: google.com
```

Meaning:

> "Please send me the homepage of Google."

```text
Browser
   ↓
HTTP Request
   ↓
Google Server
```

---

# Step 6: Server

A server is a computer that receives requests and sends responses.

Google's server receives the request and processes it.

The server decides:

* Who is requesting?
* What page is needed?
* What data should be returned?

```text
Browser
   ↓
Server
```

---

# Step 7: Database

Many websites store information inside databases.

Examples:

* User accounts
* Passwords
* Emails
* Posts
* Comments
* Videos

When you search for something on Google, the server may retrieve information from databases and other systems.

```text
Server
   ↓
Database
   ↓
Data Retrieved
```

---

# Step 8: HTTP Response

The server sends the result back to the browser.

Example:

```http
HTTP/1.1 200 OK
Content-Type: text/html
```

The response may contain:

* HTML
* CSS
* JavaScript
* Images
* Videos

```text
Server
   ↓
HTTP Response
   ↓
Browser
```

---

# Step 9: Browser Renders the Page

The browser receives the response and displays the webpage.

```text
HTML
CSS
JavaScript
   ↓
Rendered Webpage
```

You finally see:

```text
Google Search Page
```

---

# Complete Flow

```text
User
 ↓
Browser
 ↓
DNS
 ↓
IP Address
 ↓
TCP Connection
 ↓
HTTP Request
 ↓
Server
 ↓
Database
 ↓
HTTP Response
 ↓
Browser
 ↓
Webpage Displayed
```

---

# Real-Life Analogy

Imagine ordering food from a restaurant.

```text
You
 ↓
Waiter
 ↓
Kitchen
 ↓
Cooks Food
 ↓
Waiter
 ↓
Food Delivered
```

Internet version:

```text
You
 ↓
Browser
 ↓
Internet
 ↓
Server
 ↓
Database
 ↓
Server
 ↓
Browser
 ↓
Webpage
```

---

# Key Terms

| Term       | Meaning                               |
| ---------- | ------------------------------------- |
| Browser    | Software used to access websites      |
| DNS        | Converts domain names to IP addresses |
| IP Address | Unique address of a device            |
| TCP        | Creates a reliable connection         |
| HTTP       | Protocol for web communication        |
| Server     | Receives requests and sends responses |
| Database   | Stores application data               |

---

# Summary

When you type:

```text
google.com
```

the browser:

1. Finds Google's IP using DNS.
2. Creates a TCP connection.
3. Sends an HTTP request.
4. Google's server processes the request.
5. The server fetches data from databases if required.
6. The server sends an HTTP response.
7. The browser renders the webpage.

This entire process usually happens in less than a second.

