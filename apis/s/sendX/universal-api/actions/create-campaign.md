# SendX: Create Campaign



```
POST https://connect.mindcloud.co/v1/universal/sendX/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "subject": "string",
  "sender": "string",
  "htmlCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendX/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "subject": "string",
    "sender": "string",
    "htmlCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `subject` | string | yes |  |
| `sender` | string | yes |  |
| `htmlCode` | string | yes |  |
| `previewText` | string | no |  |
| `scheduleType` | number | no |  |
| `includedLists[]` | array<string> | no |  |
| `includedTags[]` | array<string> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `plainText` | string | no |  |
| `scheduleCondition` | string | no |  |
| `timeCondition` | string | no |  |
| `timezone` | string | no |  |
| `preferredTimezone` | string | no |  |
| `preferredTimeCondition` | string | no |  |
| `sendInContactsTimezone` | boolean | no |  |
| `smartSend` | boolean | no |  |
| `includedSegments[]` | array<string> | no |  |
| `excludedSegments[]` | array<string> | no |  |
| `excludedLists[]` | array<string> | no |  |
| `excludedTags[]` | array<string> | no |  |

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

Through the native SendX API, this operation is `POST /campaign` (base URL `https://api.sendx.io/api/v1/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

