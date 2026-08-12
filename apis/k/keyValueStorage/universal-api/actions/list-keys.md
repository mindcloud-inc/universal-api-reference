# Key Value Storage: List Keys

Returns one row per key stored in a namespace, ordered by key. Values are not included; read them with Get Value.

```
GET https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/list-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Key Value Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/list-keys?connectionId=$CONNECTION_ID&namespace=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespace": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/list-keys?${params}`, {
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
| `namespace` | list | yes |  |
| `limit` | number | no | Maximum keys to return. Defaults to 1000, capped at 5000. |
| `offset` | number | no | Number of keys to skip. Combine with Limit to page through a large namespace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "string",
      "key": "string",
      "namespace": "Ava Chen",
      "updatedOn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | string |  |
| `key` | string |  |
| `namespace` | string |  |
| `updatedOn` | string |  |

## Native endpoint

Through the native Key Value Storage API, this operation is `GET`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-keys.md) for the provider-specific parameters and requirements.

