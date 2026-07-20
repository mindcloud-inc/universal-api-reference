# Create API namespace with Unkey

Creates a new API namespace in Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/apis.createApi`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Create API namespace](https://unkey.com/docs/api-reference/apis/create-api-namespace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Unique identifier for this API namespace within your workspace. |
