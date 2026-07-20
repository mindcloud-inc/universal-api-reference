# Blooio Messaging: Get Current Authentication Context

Retrieves the current authentication context from Blooio Messaging.

```
GET https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-current-authentication-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blooio Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-current-authentication-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-current-authentication-context?${params}`, {
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
      "apiKey": "string",
      "authType": "string",
      "devices": [
        {}
      ],
      "integrationDetails": {},
      "metadata": {},
      "organization": {},
      "organizationId": "string",
      "usage": {},
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string |  |
| `authType` | string |  |
| `devices` | array<object> |  |
| `integrationDetails` | object |  |
| `metadata` | object |  |
| `organization` | object |  |
| `organizationId` | string |  |
| `usage` | object |  |
| `valid` | boolean |  |

## Native endpoint

Through the native Blooio Messaging API, this operation is `GET /me` (base URL `https://backend.blooio.com/v2/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-authentication-context.md) for the provider-specific parameters and requirements.

