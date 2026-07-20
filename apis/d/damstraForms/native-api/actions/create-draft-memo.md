# Create Draft Memo with Damstra Forms

Creates a draft memo in Damstra Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/memos`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Draft Memo](https://sammapi.docs.apiary.io/#reference/memos/memo-collection/create-a-draft-memo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload[]` | body | `array<object>` | yes | Array of draft memo payloads. Each item follows the Damstra create draft memo request body shape. |
