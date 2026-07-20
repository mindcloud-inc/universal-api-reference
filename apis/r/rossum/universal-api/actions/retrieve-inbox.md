# Rossum: Retrieve Inbox

Retrieves an inbox from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-inbox?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-inbox?${params}`, {
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
| `inboxID` | string | no | Rossum inbox ID. |

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

Through the native Rossum API, this operation is `GET /inboxes/:inboxID` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-inbox.md) for the provider-specific parameters and requirements.

