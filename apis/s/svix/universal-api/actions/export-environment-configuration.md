# Svix: Export Environment Configuration

Exports environment configuration from Svix.

```
POST https://connect.mindcloud.co/v1/universal/svix/latest/actions/export-environment-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/svix/latest/actions/export-environment-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/export-environment-configuration', {
  method: 'POST',
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
      "connectors": [
        {}
      ],
      "createdAt": "string",
      "eventTypes": [
        {}
      ],
      "settings": {},
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectors` | array<object> |  |
| `createdAt` | string |  |
| `eventTypes` | array<object> |  |
| `settings` | object |  |
| `version` | number |  |

## Native endpoint

Through the native Svix API, this operation is `POST /api/v1/environment/export` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-environment-configuration.md) for the provider-specific parameters and requirements.

