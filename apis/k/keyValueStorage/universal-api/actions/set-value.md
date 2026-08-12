# Key Value Storage: Set Value



```
PUT https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/set-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Key Value Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/set-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/set-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `namespace` | string | no |  |
| `key` | string | no |  |
| `value` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "namespace": "Ava Chen",
      "updatedOn": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `namespace` | string |  |
| `updatedOn` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Key Value Storage API, this operation is `GET`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-value.md) for the provider-specific parameters and requirements.

