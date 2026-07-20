# Nango: Patch Connection



```
PUT https://connect.mindcloud.co/v1/universal/nango/latest/actions/patch-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nango `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nango/latest/actions/patch-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nango/latest/actions/patch-connection', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "connectionId": "string",
      "metadata": {},
      "provider": "string",
      "providerConfigKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionId` | string |  |
| `metadata` | object |  |
| `provider` | string |  |
| `providerConfigKey` | string |  |

## Native endpoint

Through the native Nango API, this operation is `PATCH /connections/:connectionId` (base URL `https://api.nango.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-connection.md) for the provider-specific parameters and requirements.

