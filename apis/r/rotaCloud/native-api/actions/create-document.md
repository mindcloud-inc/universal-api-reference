# Create Document with RotaCloud

Creates a document in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Create Document](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | body | `string` | yes | Storage bucket containing the file. |
| `key` | body | `string` | yes | Storage key of the file. |
| `name` | body | `string` | yes | Document name. |
