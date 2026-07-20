# Verify Sudoku String with Shadify

Retrieves a Sudoku validation result from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/sudoku/verifier`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Verify Sudoku String](https://shadify.yurace.pro/modules/sudoku.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task` | query | `string` | yes | Required Sudoku rows joined by dashes, such as 123-123-123. |
