# Key Value Storage: List Namespaces

Returns every namespace that currently holds at least one key, with the number of keys in each.

```
GET https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/list-namespaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Key Value Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/list-namespaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/list-namespaces?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "keyCount": 1,
      "namespace": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keyCount` | number |  |
| `namespace` | string |  |

## Native endpoint

Through the native Key Value Storage API, this operation is `GET`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-namespaces.md) for the provider-specific parameters and requirements.

