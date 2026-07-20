# Set Client Active Status with Callingly

Updates a client's active status in Callingly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/clients/{{id}}/active`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Set Client Active Status](https://help.callingly.com/article/38-callingly-api-documentation#activate-deactivate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Callingly client ID to activate or deactivate. |
| `is_active` | body | `number` | yes | Set to 1 to activate or 0 to deactivate the client. |
