# Digital Samba: Get session statistics

Retrieves session statistics from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-session-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-session-statistics?connectionId=$CONNECTION_ID&session=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "session": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-session-statistics?${params}`, {
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
| `session` | string | yes | Session path parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metrics` | string | no | Metrics in the result dataset, set field names under comma (Ex: participation_minutes,broadcasted_minutes,subscribed_minutes). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeParticipants": 1,
      "broadcastedMinutes": 1,
      "desktopParticipationMinutes": 1,
      "liveParticipants": 1,
      "mobileParticipationMinutes": 1,
      "participationMinutes": 1,
      "roomDescription": "string",
      "roomExternalId": "string",
      "roomFriendlyUrl": "https://example.com",
      "roomId": "string",
      "roomIsDeleted": true,
      "roomMaxParticipants": 1,
      "roomPrivacy": "string",
      "roomSource": "string",
      "screenBroadcastedMinutes": 1,
      "screenSubscribedMinutes": 1,
      "sessionDuration": 1,
      "sessionEndTime": "string",
      "sessionId": "string",
      "sessionLive": true,
      "sessionStartTime": "string",
      "smarttvParticipationMinutes": 1,
      "subscribedMinutes": 1,
      "tabletParticipationMinutes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeParticipants` | number |  |
| `broadcastedMinutes` | number |  |
| `desktopParticipationMinutes` | number |  |
| `liveParticipants` | number |  |
| `mobileParticipationMinutes` | number |  |
| `participationMinutes` | number |  |
| `roomDescription` | string |  |
| `roomExternalId` | string |  |
| `roomFriendlyUrl` | string |  |
| `roomId` | string |  |
| `roomIsDeleted` | boolean |  |
| `roomMaxParticipants` | number |  |
| `roomPrivacy` | string |  |
| `roomSource` | string |  |
| `screenBroadcastedMinutes` | number |  |
| `screenSubscribedMinutes` | number |  |
| `sessionDuration` | number |  |
| `sessionEndTime` | string |  |
| `sessionId` | string |  |
| `sessionLive` | boolean |  |
| `sessionStartTime` | string |  |
| `smarttvParticipationMinutes` | number |  |
| `subscribedMinutes` | number |  |
| `tabletParticipationMinutes` | number |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /sessions/:session` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-statistics.md) for the provider-specific parameters and requirements.

