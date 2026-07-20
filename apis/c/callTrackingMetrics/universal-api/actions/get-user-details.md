# CallTrackingMetrics: Get User Details

Retrieves detailed user information from CallTrackingMetrics.

```
GET https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-user-details?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-user-details?${params}`, {
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
| `userId` | string | yes | The CallTrackingMetrics user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "language": "string",
      "lastName": "Chen",
      "liveCalls": [
        [
          "string"
        ]
      ],
      "recordingAccessSettings": {
        "passwordProtected": true,
        "status": true,
        "voicemailOnly": true
      },
      "role": "string",
      "status": "string",
      "uid": 1,
      "url": "https://example.com",
      "useFilterV2": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `language` | string |  |
| `lastName` | string |  |
| `liveCalls[]` | array |  |
| `recordingAccessSettings` | object |  |
| `recordingAccessSettings.passwordProtected` | boolean |  |
| `recordingAccessSettings.status` | boolean |  |
| `recordingAccessSettings.voicemailOnly` | boolean |  |
| `role` | string |  |
| `status` | string |  |
| `uid` | number |  |
| `url` | string |  |
| `useFilterV2` | boolean |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `GET /accounts/:accountId/users/:userId.json` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-details.md) for the provider-specific parameters and requirements.

