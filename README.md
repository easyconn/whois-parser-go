# whois-parser.go

whois-parser-go is a simple Go module for whois info parser.

## Overview

It will parse the provided whois information and return a readable data struct.

*Works for most domain extensions most of the time.*

## Installation

    go get github.com/easyconn/whois-parser-go

## Importing

    import (
        "github.com/easyconn/whois-parser-go"
    )

## Documentation

    func Parser(whois string) (whois_info WhoisInfo, err error)

## Example

    result, err := whois_parser.Parser(whois_raw)
    if err == nil {
        // Print the domain status
        fmt.Println(result.Registrar.DomainStatus)

        // Print the domain created date
        fmt.Println(result.Registrar.CreatedDate)

        // Print the domain expiration date
        fmt.Println(result.Registrar.ExpirationDate)

        // Print the registrant name
        fmt.Println(result.Registrant.Name)

        // Print the registrant email address
        fmt.Println(result.Registrant.Email)
    }

## LICENSE

Copyright 2014, Kexian Li

Apache License, Version 2.0

## Whois info query in Go

Please refer to [whois-go](https://github.com/easyconn/whois-go)

## About

- [Kexian Li](http://github.com/likexian)
- [http://www.likexian.com/](http://www.likexian.com/)
