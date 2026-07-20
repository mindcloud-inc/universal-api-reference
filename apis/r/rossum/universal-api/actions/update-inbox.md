# Rossum: Update Inbox

Updates an inbox in Rossum.

```
PUT https://connect.mindcloud.co/v1/universal/rossum/latest/actions/update-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/update-inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxID": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rossum/latest/actions/update-inbox', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxID": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboxID` | number | yes | Rossum inbox ID. |
| `name` | string | no | Updated inbox name. |
| `queue` | string | no | Inbox queue URL. |
| `queues` | list<string> | no | Inbox queue URLs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounceDeletedAnnotations": true,
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

Through the native Rossum API, this operation is `PATCH /inboxes/:inboxID` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inbox.md) for the provider-specific parameters and requirements.

