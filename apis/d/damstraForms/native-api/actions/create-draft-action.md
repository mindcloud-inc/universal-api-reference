# Create Draft Action with Damstra Forms

Creates a draft action in Damstra Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Draft Action](https://sammapi.docs.apiary.io/#reference/actions/action-collection/create-a-draft-action)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload[]` | body | `array<object>` | yes | Array of draft action payloads. Each item follows the Damstra create draft action request body shape. |
