# Rossum: Create Inbox

Creates a new inbox in Rossum.

```
POST https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "emailPrefix": "ava@example.com",
  "queue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-inbox', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "emailPrefix": "ava@example.com",
    "queue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the inbox to create. |
| `emailPrefix` | string | yes | Email prefix used to generate the Rossum inbox address. |
| `queue` | string | yes | Queue URL that should receive inbox documents. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounceDeletedAnnotations": true,
      "bounceEmailTo": {},
      "bounceEmailWithNoAttachments": true,
      "bouncePostponedAnnotations": true,
      "bounceUnprocessableAttachments": true,
      "dmarcCheckAction": "string",
      "email": "ava@example.com",
      "emailPrefix": "ava@example.com",
      "filters": {
        "documentRejectionConditions": {
          "enabled": true,
          "fileNameRegexes": {},
          "fileSizeLessThanB": {},
          "mimeTypes": [
            "string"
          ],
          "resolutionLowerThanPx": [
            1
          ]
        }
      },
      "id": 1,
      "modifiedAt": "string",
      "modifiedBy": "string",
      "name": "Ava Chen",
      "queues": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounceDeletedAnnotations` | boolean |  |
| `bounceEmailTo` | object |  |
| `bounceEmailWithNoAttachments` | boolean |  |
| `bouncePostponedAnnotations` | boolean |  |
| `bounceUnprocessableAttachments` | boolean |  |
| `dmarcCheckAction` | string |  |
| `email` | string |  |
| `emailPrefix` | string |  |
| `filters.documentRejectionConditions.enabled` | boolean |  |
| `filters.documentRejectionConditions.fileNameRegexes` | object |  |
| `filters.documentRejectionConditions.fileSizeLessThanB` | object |  |
| `filters.documentRejectionConditions.mimeTypes[]` | string |  |
| `filters.documentRejectionConditions.resolutionLowerThanPx[]` | number |  |
| `id` | number |  |
| `modifiedAt` | string |  |
| `modifiedBy` | string |  |
| `name` | string |  |
| `queues[]` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `POST /inboxes` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inbox.md) for the provider-specific parameters and requirements.

