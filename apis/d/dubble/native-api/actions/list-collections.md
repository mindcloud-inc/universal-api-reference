# List Collections with Dubble

Retrieves a list of collections from Dubble.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections`
- **Base URL:** `https://api.dubble.so/v1`
- **Official documentation:** [List Collections](https://dubble.readme.io/reference/getcollections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search for collections by name |
| `sort` | query | `string` | no | Sort direction: asc or desc |
| `sortBy` | query | `string` | no | Sort collections by created_at or updated_at |
