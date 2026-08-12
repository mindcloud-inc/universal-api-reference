# Key Value Storage: Universal API

Key Value Storage through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/keyValueStorage/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Value](actions/get-value.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/get-value?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Namespace

| Action | Method | Description |
| --- | --- | --- |
| [List Namespaces](actions/list-namespaces.md) | GET | Returns every namespace that currently holds at least one key, with the number of keys in each. |
| [Remove Namespace](actions/remove-namespace.md) | DELETE | Deletes every key stored in a namespace and returns how many were removed. This cannot be undone. |

### Value

| Action | Method | Description |
| --- | --- | --- |
| [Get Value](actions/get-value.md) | GET |  |
| [List Keys](actions/list-keys.md) | GET | Returns one row per key stored in a namespace, ordered by key. Values are not included; read them with Get Value. |
| [Remove Key](actions/remove-key.md) | DELETE | Deletes one key and its value from a namespace so the row no longer occupies storage. Returns deleted: false when the key did not exist. |
| [Set Value](actions/set-value.md) | PUT |  |

