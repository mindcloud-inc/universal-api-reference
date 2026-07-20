# Verify Sudoku Grid with Shadify

Retrieves a Sudoku validation result from Shadify.

## Endpoint

- **Method:** `POST`
- **Path:** `/sudoku/verifier`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Verify Sudoku Grid](https://shadify.yurace.pro/modules/sudoku.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task[]` | body | `array<array>` | yes | Required solved Sudoku grid as a 9x9 array of numbers. |
