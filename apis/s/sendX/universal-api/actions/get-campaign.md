# SendX: Get Campaign



```
GET https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-campaign?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-campaign?${params}`, {
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
| `identifier` | string | no | The SendX campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignScreenshotUrl": "https://example.com",
      "excludedLists": [
        "string"
      ],
      "excludedSegments": [
        "string"
      ],
      "excludedTags": [
        "string"
      ],
      "id": "string",
      "includedLists": [
        "string"
      ],
      "includedSegments": [
        "string"
      ],
      "includedTags": [
        "string"
      ],
      "isArchived": true,
      "name": "Ava Chen",
      "preferredTimeCondition": "string",
      "preferredTimezone": "string",
      "scheduleCondition": "string",
      "scheduleType": 1,
      "sender": "string",
      "sendInContactsTimezone": true,
      "smartSend": true,
      "status": 1,
      "strategy": "string",
      "subject": "string",
      "timeCondition": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignScreenshotUrl` | string |  |
| `excludedLists` | array<string> |  |
| `excludedSegments` | array<string> |  |
| `excludedTags` | array<string> |  |
| `id` | string |  |
| `includedLists` | array<string> |  |
| `includedSegments` | array<string> |  |
| `includedTags` | array<string> |  |
| `isArchived` | boolean |  |
| `name` | string |  |
| `preferredTimeCondition` | string |  |
| `preferredTimezone` | string |  |
| `scheduleCondition` | string |  |
| `scheduleType` | number |  |
| `sender` | string |  |
| `sendInContactsTimezone` | boolean |  |
| `smartSend` | boolean |  |
| `status` | number |  |
| `strategy` | string |  |
| `subject` | string |  |
| `timeCondition` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native SendX API, this operation is `GET /campaign/:identifier` (base URL `https://api.sendx.io/api/v1/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

