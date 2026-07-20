# GMass: Send Campaign From Draft

Creates and sends a GMass campaign from a draft.

```
POST https://connect.mindcloud.co/v1/universal/gMass/latest/actions/send-campaign-from-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/send-campaign-from-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignDraftId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gMass/latest/actions/send-campaign-from-draft', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignDraftId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignDraftId` | string | yes |  |
| `createDrafts` | boolean | no |  |
| `friendlyName` | string | no |  |
| `openTracking` | boolean | no |  |
| `clickTracking` | boolean | no |  |
| `sendTime` | string | no |  |
| `previewText` | string | no |  |
| `replyTo` | string | no |  |
| `fromName` | string | no |  |
| `verify` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "creationTime": "2026-05-07T12:00:00.000Z",
      "friendlyName": "Ava Chen",
      "fromLine": "string",
      "stage": 1,
      "statistics": {
        "blocks": 1,
        "bounces": 1,
        "clicks": 1,
        "opens": 1,
        "recipients": 1,
        "replies": 1,
        "unsubscribes": 1
      },
      "status": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number |  |
| `creationTime` | date |  |
| `friendlyName` | string |  |
| `fromLine` | string |  |
| `stage` | number |  |
| `statistics.blocks` | number |  |
| `statistics.bounces` | number |  |
| `statistics.clicks` | number |  |
| `statistics.opens` | number |  |
| `statistics.recipients` | number |  |
| `statistics.replies` | number |  |
| `statistics.unsubscribes` | number |  |
| `status` | string |  |
| `subject` | string |  |

## Native endpoint

Through the native GMass API, this operation is `POST /campaigns/:campaignDraftId` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-campaign-from-draft.md) for the provider-specific parameters and requirements.

