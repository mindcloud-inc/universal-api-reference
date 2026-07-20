# Recallai: Update Calendar

Updates an existing calendar in Recallai.

```
PUT https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calendarId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-calendar', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calendarId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calendarId` | string | yes | A UUID string identifying this calendar. |
| `oauthClientId` | string | no | Oauth Client ID |
| `oauthClientSecret` | string | no | Oauth Client Secret |
| `oauthEmail` | string | no | Oauth Email |
| `oauthRefreshToken` | string | no | Oauth Refresh Token |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "metadata": {},
      "oauthClientId": "string",
      "oauthClientSecret": "string",
      "oauthEmail": "ava@example.com",
      "oauthRefreshToken": "string",
      "platform": "string",
      "platformEmail": "ava@example.com",
      "status": "string",
      "statusChanges": [
        {}
      ],
      "updatedAt": "string",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `oauthClientId` | string |  |
| `oauthClientSecret` | string |  |
| `oauthEmail` | string |  |
| `oauthRefreshToken` | string |  |
| `platform` | string |  |
| `platformEmail` | string |  |
| `status` | string |  |
| `statusChanges` | array<object> |  |
| `updatedAt` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Recallai API, this operation is `PATCH /api/v2/calendars/:id/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-calendar.md) for the provider-specific parameters and requirements.

