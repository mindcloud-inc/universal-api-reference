# Run a Formula with Quickbase

Evaluates a Quickbase formula and returns the result.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/formula/run`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Run a Formula](https://developer.quickbase.com/operation/runFormula)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The Quickbase table identifier. |
| `formula` | body | `string` | yes | The Quickbase formula to run. |
| `rid` | body | `number` | no | Optional record ID for formulas that require record context. |
