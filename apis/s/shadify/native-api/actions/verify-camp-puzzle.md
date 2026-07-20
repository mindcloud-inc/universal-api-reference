# Verify Camp Puzzle with Shadify

Retrieves a Camp validation result from Shadify.

## Endpoint

- **Method:** `POST`
- **Path:** `/camp/verifier`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Verify Camp Puzzle](https://shadify.yurace.pro/modules/camp.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rowTents[]` | body | `array<number>` | yes | Required array of tent counts for each row. |
| `columnTents[]` | body | `array<number>` | yes | Required array of tent counts for each column. |
| `solution[]` | body | `array<array>` | yes | Required completed Camp grid, where 1 values are trees and 2 values are tents. |
