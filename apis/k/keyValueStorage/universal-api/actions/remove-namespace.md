# Key Value Storage: Remove Namespace

Deletes every key stored in a namespace and returns how many were removed. This cannot be undone.

```
DELETE https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/remove-namespace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Key Value Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/remove-namespace?connectionId=$CONNECTION_ID&namespace=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespace": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/remove-namespace?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedCount": 1,
      "namespace": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedCount` | number |  |
| `namespace` | string |  |

## Native endpoint

Through the native Key Value Storage API, this operation is `GET`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-namespace.md) for the provider-specific parameters and requirements.

