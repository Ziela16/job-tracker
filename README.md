
<h1 align="center">Job-Tracker </h1>

<p align="center"> Personal, mini-project. The main purpose of this app is to store job application from multiple job boards, so you never apply twice for the same position.   </p>

<h2 align="center"> Current project status </h2> 
<p align="center"> <font color="FF0000">  <b> Work in progress  </b> </font> </p>

## The problem

As a person who looks for a job across multiple websites, I often lose track whether I've already applied. Many websites, many job offers, many duplicates. It's just easy to get lost.

## Solution

One place for all your applications. Many QoL functions to make job-hunting less chaotic.


## Features

- Advanced job applications list
- Repeated application detector
- Configurable auto archive for obsolete applications
- Export/Import options
- NO AI functions.


## Requirements

- Docker (recommended)
- PHP 8.4 (included in dockerfile)
- MariaDB 10.11 (included in dockerfile)
- Composer ((included in dockerfile))

## Optional

- mkcert

## Setup Guide

### DEFAULT (non https)

1. **Make hosts entry for url:**

<code> 127.0.0.1      job-tracker.test </code>

| Operating System | Hosts file localisation               |
| ---------------- | ------------------------------------- |
| Windows          | C:\Windows\System32\drivers\etc\hosts |

2. **Copy .env.example and configure it**
3. **Do compose up, generate app key and make migrations**

### With HTTPS

1. **Make host entry**
2. **Install mkcert on windows side, https://github.com/filosottile/mkcert**
3. **Go to "docker/development/nginx/certs" and do "mkcert job-tracker.test"**
4. **Copy .env.example, configure it with uncommenting COMPOSE_FILE variable**
5. **Change APP_URL to https:// instead of http://**
6. **Do compose up, generate app key and make migrations**


## DISCLAIMER

<font color="FF0000"> This project does not contain any code written by AI.</font>
