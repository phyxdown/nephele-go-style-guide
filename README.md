# Nephele Go Style Guide

This style guide outlines the coding conventions of Nephele team.

## Background

Nephele is a complete solution to enterprise multimedia needs. Go is one of the main development language used by most of Nephele team members. The very go language is simple, powerful and probably a most officially restricted language, yet still used in a relatively smaller range. Thus in some common cases, we still lack rules and conventions intended to prevent obstacles of team efficiency and barriers to learning.

## Goals of the Style Guide

**No conflict with go fmt tool**

**Optimize for the reader, not the writer**

**Avoid tricky realization**

**Be mindful of scale**

**No impact on interface**

**Concede to optimization when necessary**

## Table of Contents

* [How to Import Package](#how-to-import-package)


## How to Import Package

**For example:**
```go
    import (
        time_p "time"
        http_p "net/http"
    )
```

**Not:**
```go
    import (
        "time"
        "net/http"
    )
```

**Not:**
```go
    import "time"
    import "net/http"
```

## Indent

Indentation MUST use tabs.


## Variables

A suffixed filename is needed for global private variable or const.

**For example:**
```go
    //foo.go
    var a_foo int
    func b() {
        ...
    }
```

**Not:**
```go
    //foo.go
    var a int
    func b() {
        ...
    }
```


## Functions

Global functions are only allowed in the file whose package has the same name.

**Allowed:**
```go
    package foo
    //foo.go

    func A() {
        ...
    }

    func a() {
        ...
    }
```

**Banned:**
```go
    package foo
    //goo.go

    func B() {
        ...
    }

    func b() {
        ...
    }
```

