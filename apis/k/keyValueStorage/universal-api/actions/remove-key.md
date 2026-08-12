# Key Value Storage: Remove Key

Deletes one key and its value from a namespace so the row no longer occupies storage. Returns deleted: false when the key did not exist.

```
DELETE https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/remove-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Key Value Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/remove-key?connectionId=$CONNECTION_ID&namespace=Ava%20Chen&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespace": "Ava Chen",
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/remove-key?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `namespace` | string | yes |  |
| `key` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "key": "string",
      "namespace": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `key` | string |  |
| `namespace` | string |  |

## Native endpoint

Through the native Key Value Storage API, this operation is `GET`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-key.md) for the provider-specific parameters and requirements.

