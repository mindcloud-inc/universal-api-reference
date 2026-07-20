# Shadify: Native API Reference

A consolidated summary of Shadify's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://shadify.yurace.pro/documentation.html
- **API base URL:** `https://shadify.yurace.pro/api`

## Authentication

### No authentication

Shadify public REST endpoints do not require registration, API keys, or OAuth credentials.

This API does not require request authentication.

[Official authentication documentation](https://shadify.yurace.pro/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Addition Expression](actions/generate-addition-expression.md) | `GET /math/add` | [docs](https://shadify.yurace.pro/modules/math.html) |
| [Generate Anagram](actions/generate-anagram.md) | `GET /anagram/generator` | [docs](https://shadify.yurace.pro/modules/anagram.html) |
| [Generate Camp Puzzle](actions/generate-camp-puzzle.md) | `GET /camp/generator` | [docs](https://shadify.yurace.pro/modules/camp.html) |
| [Generate Capital Quiz](actions/generate-capital-quiz.md) | `GET /countries/capital-quiz` | [docs](https://shadify.yurace.pro/modules/countries.html) |
| [Generate Country Quiz](actions/generate-country-quiz.md) | `GET /countries/country-quiz` | [docs](https://shadify.yurace.pro/modules/countries.html) |
| [Generate Division Expression](actions/generate-division-expression.md) | `GET /math/div` | [docs](https://shadify.yurace.pro/modules/math.html) |
| [Generate Kuromasu Puzzle](actions/generate-kuromasu-puzzle.md) | `GET /kuromasu/generator` | [docs](https://shadify.yurace.pro/modules/kuromasu.html) |
| [Generate Memory Grid](actions/generate-memory-grid.md) | `GET /memory/generator` | [docs](https://shadify.yurace.pro/modules/memory.html) |
| [Generate Minesweeper Field](actions/generate-minesweeper-field.md) | `GET /minesweeper/generator` | [docs](https://shadify.yurace.pro/modules/minesweeper.html) |
| [Generate Multiplication Expression](actions/generate-multiplication-expression.md) | `GET /math/mul` | [docs](https://shadify.yurace.pro/modules/math.html) |
| [Generate Quadratic Equation](actions/generate-quadratic-equation.md) | `GET /math/quad` | [docs](https://shadify.yurace.pro/modules/math.html) |
| [Generate Schulte Table](actions/generate-schulte-table.md) | `GET /schulte/generator` | [docs](https://shadify.yurace.pro/modules/schulte.html) |
| [Generate Subtraction Expression](actions/generate-subtraction-expression.md) | `GET /math/sub` | [docs](https://shadify.yurace.pro/modules/math.html) |
| [Generate Sudoku Puzzle](actions/generate-sudoku-puzzle.md) | `GET /sudoku/generator` | [docs](https://shadify.yurace.pro/modules/sudoku.html) |
| [Generate Takuzu Puzzle](actions/generate-takuzu-puzzle.md) | `GET /takuzu/generator` | [docs](https://shadify.yurace.pro/modules/takuzu.html) |
| [Generate Word Search Grid](actions/generate-word-search-grid.md) | `GET /wordsearch/generator` | [docs](https://shadify.yurace.pro/modules/wordsearch.html) |
| [Load Set Game State](actions/load-set-game-state.md) | `GET /set/:state` | [docs](https://shadify.yurace.pro/modules/set.html) |
| [Start Set Game](actions/start-set-game.md) | `GET /set/start` | [docs](https://shadify.yurace.pro/modules/set.html) |
| [Verify Camp Puzzle](actions/verify-camp-puzzle.md) | `POST /camp/verifier` | [docs](https://shadify.yurace.pro/modules/camp.html) |
| [Verify Kuromasu Puzzle](actions/verify-kuromasu-puzzle.md) | `POST /kuromasu/verifier` | [docs](https://shadify.yurace.pro/modules/kuromasu.html) |
| [Verify Sudoku Grid](actions/verify-sudoku-grid.md) | `POST /sudoku/verifier` | [docs](https://shadify.yurace.pro/modules/sudoku.html) |
| [Verify Sudoku String](actions/verify-sudoku-string.md) | `GET /sudoku/verifier` | [docs](https://shadify.yurace.pro/modules/sudoku.html) |
| [Verify Takuzu Grid](actions/verify-takuzu-grid.md) | `POST /takuzu/verifier` | [docs](https://shadify.yurace.pro/modules/takuzu.html) |
| [Verify Takuzu String](actions/verify-takuzu-string.md) | `GET /takuzu/verifier` | [docs](https://shadify.yurace.pro/modules/takuzu.html) |
