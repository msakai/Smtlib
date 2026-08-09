# Smtlib

> [!WARNING]
> This repository (a fork of the `Smtlib` library ([Hackage](https://hackage.haskell.org/package/SmtLib), [GitHub](https://github.com/MfesGA/Smtlib))) is archived and no longer maintained as of 2026-08.
> I recommend migrating to the `language-smtlib` library ([Hackage](https://hackage.haskell.org/package/language-smtlib), [GitHub](https://github.com/msakai/language-smtlib/)), which is actively maintained.

SMTLib2 parsers.

A library with SMTLib2 syntax and parsers for commands and their responses.

How to parse a smtlib2 file:
```Haskell
import Smtlib.Parsers.CommandsParsers
import Smtlib.Syntax.Syntax
import Text.ParserCombinators.Parsec

parseFile :: FilePath -> IO (Either ParseError Source)
parseFile x = parse parseSource "" <$> readFile x
```
