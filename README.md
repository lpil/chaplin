# Chaplin

[Mustache][mustache] text templates using Erlang's [bbmustache][bbmustache] package.

[![Package Version](https://img.shields.io/hexpm/v/chaplin)](https://hex.pm/packages/chaplin)
[![Hex Docs](https://img.shields.io/badge/hex-docs-ffaff3)](https://hexdocs.pm/chaplin/)

[mustache]: https://mustache.github.io/
[bbmustache]: https://github.com/soranoba/bbmustache

```gleam
import chaplin

pub fn main() {
  let assert Ok(template) = chaplin.compile("Hello, {{name}}!")

  let rendered = chaplin.render(template, [
    #("name", chaplin.string("World")),
  ])

  assert rendered == "Hello, World!"
}
```

Further documentation can be found at <https://hexdocs.pm/chaplin>.
