# Rossum: List Inboxes

Retrieves inboxes from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-inboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-inboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-inboxes?${params}`, {
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
| `emailPrefix` | string | no | Filter inboxes by email prefix. |
| `ordering` | string | no | Ordering expression, for example name or -name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "next": {},
        "previous": {}
      },
      "results": [
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
              "fileNameRegexes": [
                "Ava Chen"
              ],
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
          "modifiedAt": {},
          "modifiedBy": {},
          "name": "Ava Chen",
          "queues": [
            "string"
          ],
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.next` | object |  |
| `pagination.previous` | object |  |
| `results[].bounceDeletedAnnotations` | boolean |  |
| `results[].bounceEmailTo` | object |  |
| `results[].bounceEmailWithNoAttachments` | boolean |  |
| `results[].bouncePostponedAnnotations` | boolean |  |
| `results[].bounceUnprocessableAttachments` | boolean |  |
| `results[].dmarcCheckAction` | string |  |
| `results[].email` | string |  |
| `results[].emailPrefix` | string |  |
| `results[].filters.documentRejectionConditions.enabled` | boolean |  |
| `results[].filters.documentRejectionConditions.fileNameRegexes[]` | string |  |
| `results[].filters.documentRejectionConditions.fileSizeLessThanB` | object |  |
| `results[].filters.documentRejectionConditions.mimeTypes[]` | string |  |
| `results[].filters.documentRejectionConditions.resolutionLowerThanPx[]` | number |  |
| `results[].id` | number |  |
| `results[].modifiedAt` | object |  |
| `results[].modifiedBy` | object |  |
| `results[].name` | string |  |
| `results[].queues[]` | string |  |
| `results[].url` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `GET /inboxes` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inboxes.md) for the provider-specific parameters and requirements.

