# Add Sequence To Experience with Storyscale

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/experience/add-sequence/{id}`
- **Base URL:** `https://prodapi.storyscale.com/api`
- **Official documentation:** [Add Sequence To Experience](https://prodapi.storyscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Storyscale experience ID. |
| `sequence_id` | body | `string` | yes | The sequence to add to the experience. |
