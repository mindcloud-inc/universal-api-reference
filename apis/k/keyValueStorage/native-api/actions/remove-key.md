# Remove Key with Key Value Storage

Deletes one key and its value from a namespace so the row no longer occupies storage. Returns deleted: false when the key did not exist.

## Endpoint

- **Method:** `GET`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `namespace` | body | `string` | yes |
| `key` | body | `string` | yes |
