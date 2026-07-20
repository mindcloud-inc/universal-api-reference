# Recallai: Create Calendar

Creates a new calendar in Recallai.

```
POST https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "oauthClientId": "string",
  "oauthClientSecret": "string",
  "oauthRefreshToken": "string",
  "platform": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-calendar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "oauthClientId": "string",
    "oauthClientSecret": "string",
    "oauthRefreshToken": "string",
    "platform": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `oauthClientId` | string | yes | Oauth Client ID |
| `oauthClientSecret` | string | yes | Oauth Client Secret |
| `oauthEmail` | string | no | Oauth Email |
| `oauthRefreshToken` | string | yes | Oauth Refresh Token |
| `platform` | string | yes | * `google_calendar` - Google Calendar * `microsoft_outlook` - Microsoft Outlook |

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
        "string"
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
| `statusChanges` | array |  |
| `updatedAt` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Recallai API, this operation is `POST /api/v2/calendars/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-calendar.md) for the provider-specific parameters and requirements.

