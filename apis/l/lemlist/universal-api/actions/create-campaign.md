# lemlist: Create Campaign

Creates a new campaign in lemlist.

```
POST https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/create-campaign', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The name of the campaign to create. Example: `MindCloud Stage 3 Test Campaign`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "displayedVariableKeys": [
        "string"
      ],
      "emoji": "string",
      "id": "string",
      "inSequenceLeadCount": 1,
      "name": "Ava Chen",
      "reviewedCount": 1,
      "scannedCount": 1,
      "scheduleIds": [
        "string"
      ],
      "sequenceId": "string",
      "state": "string",
      "stopOnEmailReplied": true,
      "teamId": "string",
      "unsubscribe": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `displayedVariableKeys[]` | string |  |
| `emoji` | string |  |
| `id` | string |  |
| `inSequenceLeadCount` | number |  |
| `name` | string |  |
| `reviewedCount` | number |  |
| `scannedCount` | number |  |
| `scheduleIds[]` | string |  |
| `sequenceId` | string |  |
| `state` | string |  |
| `stopOnEmailReplied` | boolean |  |
| `teamId` | string |  |
| `unsubscribe` | string |  |

## Native endpoint

Through the native lemlist API, this operation is `POST /campaigns` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

