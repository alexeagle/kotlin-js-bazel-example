# Kotlin webapp built with Bazel

Kotlin is a programming language gaining adoption for writing Android applications. It can be compiled to Java Virtual Machine, LLVM intermediate code (to target C++/Objective C) and JavaScript.

See [Kotlin JavaScript Overview].

This is a tiny demonstration of combining [rules_kotlin] and [rules_nodejs]. 
Since Kotlin can produce JS, we should be able to naturally use Bazel to compose the Kotlin rules with the JS ones.

> Gradle or Maven are typically used to build Kotlin code but don't have a nodejs/web toolchain, and typical web toolchains don't support Kotlin compilation, so this is pretty novel.

Try it:

```sh
$ npm i && npm run serve
```

This should download dependencies for both Kotlin and JavaScript, compile the Kotlin code with the Kotlin compiler, then bundle up the JS application with lazy-loading and serve it with a simple HTTP server.

[rules_kotlin]: https://github.com/bazelbuild/rules_kotlin
[rules_nodejs]: https://github.com/bazelbuild/rules_nodejs
[Kotlin JavaScript Overview]: https://kotlinlang.org/docs/reference/js-overview.html
