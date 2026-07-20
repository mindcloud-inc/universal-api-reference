# Rossum: Create Annotation

Creates a new annotation in Rossum.

```
POST https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "string",
  "queue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-annotation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": "string",
    "queue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | string | yes | Document URL. |
| `queue` | string | yes | Target queue URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedAt": {},
      "automated": true,
      "automaticallyRejected": true,
      "automationBlocker": {},
      "confirmedAt": {},
      "confirmedBy": {},
      "content": "string",
      "createdAt": "string",
      "creator": "string",
      "deletedAt": {},
      "deletedBy": {},
      "document": "string",
      "einvoice": true,
      "email": {},
      "emailThread": {},
      "exportedAt": {},
      "exportedBy": {},
      "exportFailedAt": {},
      "hasEmailThreadWithNewReplies": true,
      "hasEmailThreadWithReplies": true,
      "id": 1,
      "messages": {},
      "modifiedAt": {},
      "modifiedBy": {},
      "modifier": {},
      "organization": "string",
      "prediction": {},
      "purgedAt": {},
      "purgedBy": {},
      "queue": "string",
      "rejectedAt": {},
      "rejectedBy": {},
      "restrictedAccess": true,
      "rirPollId": {},
      "schema": "string",
      "status": "string",
      "suggestedEdit": {},
      "timeSpent": 1,
      "trainingEnabled": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedAt` | object |  |
| `automated` | boolean |  |
| `automaticallyRejected` | boolean |  |
| `automationBlocker` | object |  |
| `confirmedAt` | object |  |
| `confirmedBy` | object |  |
| `content` | string |  |
| `createdAt` | string |  |
| `creator` | string |  |
| `deletedAt` | object |  |
| `deletedBy` | object |  |
| `document` | string |  |
| `einvoice` | boolean |  |
| `email` | object |  |
| `emailThread` | object |  |
| `exportedAt` | object |  |
| `exportedBy` | object |  |
| `exportFailedAt` | object |  |
| `hasEmailThreadWithNewReplies` | boolean |  |
| `hasEmailThreadWithReplies` | boolean |  |
| `id` | number |  |
| `messages` | object |  |
| `modifiedAt` | object |  |
| `modifiedBy` | object |  |
| `modifier` | object |  |
| `organization` | string |  |
| `prediction` | object |  |
| `purgedAt` | object |  |
| `purgedBy` | object |  |
| `queue` | string |  |
| `rejectedAt` | object |  |
| `rejectedBy` | object |  |
| `restrictedAccess` | boolean |  |
| `rirPollId` | object |  |
| `schema` | string |  |
| `status` | string |  |
| `suggestedEdit` | object |  |
| `timeSpent` | number |  |
| `trainingEnabled` | boolean |  |
| `url` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `POST /annotations` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-annotation.md) for the provider-specific parameters and requirements.

