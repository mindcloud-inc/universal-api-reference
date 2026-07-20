# Create Lead with Close

Creates a new lead in Close.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [Create Lead](https://developer.close.com/resources/leads/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Lead name. |
| `status_id` | body | `string` | no | Lead status ID. |
