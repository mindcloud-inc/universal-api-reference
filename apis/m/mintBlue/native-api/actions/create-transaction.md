# Create Transaction with mintBlue

Creates a new transaction in mintBlue.

## Endpoint

- **Method:** `POST`
- **Path:** `/sdk/latest`
- **Base URL:** `https://api.mintblue.com`
- **Official documentation:** [Create Transaction](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#createTransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.project_id` | body | `string` | yes | Project ID. |
| `params.outputs[]` | body | `array<object>` | yes | Transaction outputs array. |
| `params.metadata` | body | `object` | no | Optional metadata object. |
| `params.rawtx` | body | `boolean` | no | Whether to include raw transaction. |
