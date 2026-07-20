# Create Collection with Dubble

Creates a new collection in Dubble.

## Endpoint

- **Method:** `POST`
- **Path:** `/collections`
- **Base URL:** `https://api.dubble.so/v1`
- **Official documentation:** [Create Collection](https://dubble.readme.io/reference/createcollection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the collection |
| `visibility` | body | `string` | no | The visibility setting for the collection |
