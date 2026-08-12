# List Keys with Key Value Storage

Returns one row per key stored in a namespace, ordered by key. Values are not included; read them with Get Value.

## Endpoint

- **Method:** `GET`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace` | body | `list` | yes | — |
| `limit` | body | `number` | no | Maximum keys to return. Defaults to 1000, capped at 5000. |
| `offset` | body | `number` | no | Number of keys to skip. Combine with Limit to page through a large namespace. |
