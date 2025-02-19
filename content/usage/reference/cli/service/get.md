---
title: "Get"
linkTitle: "Get"
weight: 5
description: >
  Learn how to get services.
---

## Information

```sh
NAME:
   vela get service - Display a list of services

USAGE:
   vela get service [command options] [arguments...]

DESCRIPTION:
   Use this command to get a list of services.
```

## Flags

```sh
OPTIONS:
   --org value                                    Provide the organization for the repository [$BUILD_ORG]
   --repo value                                   Provide the repository contained with the organization [$BUILD_REPO]
   --build-number value, --build value, -b value  Provide the build number (default: 0) [$BUILD_NUMBER]
   --output value, -o value                       Print the output in wide, yaml or json format
```

## Examples

```sh
EXAMPLES:
 1. Get services for a build.
    $ vela get service --org github --repo octocat --build-number 1
 2. Get services for a build with wide view output.
    $ vela get service --org github --repo octocat --build-number 1 --output wide
 3. Get services for a build with yaml output.
    $ vela get service --org github --repo octocat --build-number 1 --output yaml
 4. Get services for a build with json output.
    $ vela get service --org github --repo octocat --build-number 1 --output json
 5. Get services for a build when org and repo config or environment variables are set.
    $ vela get service --number 1
```

## Sample

```sh
$ vela get service --org github --repo octocat --build-number 5

NAME            STATUS  RUNTIME DURATION
publish         failure         1s
build           success         17s
test            success         10s
clone           success         2s
```
