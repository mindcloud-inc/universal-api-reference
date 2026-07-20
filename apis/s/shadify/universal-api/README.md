# <img src="https://images.mindcloud.co/apps/icons/shadify_1777639467575.png" alt="Shadify logo" width="28" height="28"> Shadify: Universal API

Generate and validate puzzle data using the open-source Shadify public REST API, including Sudoku, Takuzu, Set, math, Schulte tables, Minesweeper, word search, anagrams, countries quizzes, Camp, Kuromasu, and memory grids.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shadify/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shadify.yurace.pro/
- **Vendor API docs:** https://shadify.yurace.pro/documentation.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Addition Expression](actions/generate-addition-expression.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-addition-expression?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Anagram

| Action | Method | Description |
| --- | --- | --- |
| [Generate Anagram](actions/generate-anagram.md) | GET | Retrieves a random anagram from Shadify. |

### Camp Puzzle

| Action | Method | Description |
| --- | --- | --- |
| [Generate Camp Puzzle](actions/generate-camp-puzzle.md) | GET | Retrieves a random Camp puzzle from Shadify. |

### Camp Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Camp Puzzle](actions/verify-camp-puzzle.md) | GET | Retrieves a Camp validation result from Shadify. |

### Country Quiz

| Action | Method | Description |
| --- | --- | --- |
| [Generate Capital Quiz](actions/generate-capital-quiz.md) | GET | Retrieves a capital quiz from Shadify. |
| [Generate Country Quiz](actions/generate-country-quiz.md) | GET | Retrieves a country quiz from Shadify. |

### Kuromasu Puzzle

| Action | Method | Description |
| --- | --- | --- |
| [Generate Kuromasu Puzzle](actions/generate-kuromasu-puzzle.md) | GET | Retrieves a random Kuromasu puzzle from Shadify. |

### Kuromasu Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Kuromasu Puzzle](actions/verify-kuromasu-puzzle.md) | GET | Retrieves a Kuromasu validation result from Shadify. |

### Math Expression

| Action | Method | Description |
| --- | --- | --- |
| [Generate Addition Expression](actions/generate-addition-expression.md) | GET | Retrieves a random addition expression from Shadify. |
| [Generate Division Expression](actions/generate-division-expression.md) | GET | Retrieves a random division expression from Shadify. |
| [Generate Multiplication Expression](actions/generate-multiplication-expression.md) | GET | Retrieves a random multiplication expression from Shadify. |
| [Generate Subtraction Expression](actions/generate-subtraction-expression.md) | GET | Retrieves a random subtraction expression from Shadify. |

### Memory Grid

| Action | Method | Description |
| --- | --- | --- |
| [Generate Memory Grid](actions/generate-memory-grid.md) | GET | Retrieves a random memory grid from Shadify. |

### Minesweeper Field

| Action | Method | Description |
| --- | --- | --- |
| [Generate Minesweeper Field](actions/generate-minesweeper-field.md) | GET | Retrieves a random Minesweeper field from Shadify. |

### Quadratic Equation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Quadratic Equation](actions/generate-quadratic-equation.md) | GET | Retrieves a random quadratic equation from Shadify. |

### Schulte Table

| Action | Method | Description |
| --- | --- | --- |
| [Generate Schulte Table](actions/generate-schulte-table.md) | GET | Retrieves a random Schulte table from Shadify. |

### Set Game

| Action | Method | Description |
| --- | --- | --- |
| [Load Set Game State](actions/load-set-game-state.md) | GET | Retrieves a Set game state from Shadify. |
| [Start Set Game](actions/start-set-game.md) | GET | Retrieves a new Set game state from Shadify. |

### Sudoku Puzzle

| Action | Method | Description |
| --- | --- | --- |
| [Generate Sudoku Puzzle](actions/generate-sudoku-puzzle.md) | GET | Retrieves a random Sudoku puzzle from Shadify. |

### Sudoku Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Sudoku Grid](actions/verify-sudoku-grid.md) | GET | Retrieves a Sudoku validation result from Shadify. |
| [Verify Sudoku String](actions/verify-sudoku-string.md) | GET | Retrieves a Sudoku validation result from Shadify. |

### Takuzu Puzzle

| Action | Method | Description |
| --- | --- | --- |
| [Generate Takuzu Puzzle](actions/generate-takuzu-puzzle.md) | GET | Retrieves a random Takuzu puzzle from Shadify. |

### Takuzu Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Takuzu Grid](actions/verify-takuzu-grid.md) | GET | Retrieves a Takuzu validation result from Shadify. |
| [Verify Takuzu String](actions/verify-takuzu-string.md) | GET | Retrieves a Takuzu validation result from Shadify. |

### Word Search Grid

| Action | Method | Description |
| --- | --- | --- |
| [Generate Word Search Grid](actions/generate-word-search-grid.md) | GET | Retrieves a random word search grid from Shadify. |

