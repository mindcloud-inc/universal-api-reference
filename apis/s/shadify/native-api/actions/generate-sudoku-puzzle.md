# Generate Sudoku Puzzle with Shadify

Retrieves a random Sudoku puzzle from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/sudoku/generator`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Sudoku Puzzle](https://shadify.yurace.pro/modules/sudoku.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fill` | query | `number` | no | Optional fill level from 0 to 50 percent. Default is 30. |
