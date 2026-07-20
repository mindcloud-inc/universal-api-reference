# Delete Stacks with Digit.ink

## Endpoint

- **Method:** `DELETE`
- **Path:** `/stacks`
- **Base URL:** `https://app.digit.ink/api/v1`
- **Official documentation:** [Delete Stacks](https://app.digit.ink/api/v1/classic-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuids[]` | query | `array<string>` | yes | Array of stack UUIDs to delete. |
