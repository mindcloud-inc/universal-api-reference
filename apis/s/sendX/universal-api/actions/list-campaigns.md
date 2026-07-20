# SendX: List Campaigns



```
GET https://connect.mindcloud.co/v1/universal/sendX/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendX `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendX/latest/actions/list-campaigns?${params}`, {
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
| `campaignType` | string | no | Filter campaigns by type: all, draft, scheduled, or sent. |

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

Through the native SendX API, this operation is `GET /campaign` (base URL `https://api.sendx.io/api/v1/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

