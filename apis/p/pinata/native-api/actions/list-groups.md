# List Groups with Pinata

Retrieves groups from Pinata for a selected network.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/groups/:network`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [List Groups](https://docs.pinata.cloud/api-reference/endpoint/list-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
