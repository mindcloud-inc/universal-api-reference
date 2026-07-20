# Rossum: Search Annotations

Finds annotations in Rossum using a complex filter.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/search-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/search-annotations?connectionId=$CONNECTION_ID&queryString.string=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queryString.string": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/search-annotations?${params}`, {
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
| `queryString.string` | string | yes | Full-text search term (minimum 2 characters). |
| `pageSize` | number | no | Number of results per page (max 500). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "next": {},
        "previous": {},
        "total": 1,
        "totalPages": 1
      },
      "results": [
        {
          "assignedAt": {},
          "automated": true,
          "automaticallyRejected": true,
          "automationBlocker": "string",
          "confirmedAt": {},
          "confirmedBy": {},
          "content": "string",
          "createdAt": "string",
          "creator": {},
          "deletedAt": {},
          "deletedBy": {},
          "document": "string",
          "einvoice": true,
          "email": "ava@example.com",
          "emailThread": "ava@example.com",
          "exportedAt": {},
          "exportedBy": {},
          "exportFailedAt": {},
          "hasEmailThreadWithNewReplies": true,
          "hasEmailThreadWithReplies": true,
          "id": 1,
          "modifiedAt": {},
          "modifiedBy": {},
          "modifier": {},
          "organization": "string",
          "pages": [
            "string"
          ],
          "prediction": {
            "source": "string",
            "version": {}
          },
          "purgedAt": {},
          "purgedBy": {},
          "queue": "string",
          "rejectedAt": {},
          "rejectedBy": {},
          "relatedEmails": [
            "ava@example.com"
          ],
          "relations": [
            "string"
          ],
          "restrictedAccess": true,
          "rirPollId": "string",
          "schema": "string",
          "status": "string",
          "suggestedEdit": {},
          "timeSpent": 1,
          "trainingEnabled": true,
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
| `pagination.total` | number |  |
| `pagination.totalPages` | number |  |
| `results[].assignedAt` | object |  |
| `results[].automated` | boolean |  |
| `results[].automaticallyRejected` | boolean |  |
| `results[].automationBlocker` | string |  |
| `results[].confirmedAt` | object |  |
| `results[].confirmedBy` | object |  |
| `results[].content` | string |  |
| `results[].createdAt` | string |  |
| `results[].creator` | object |  |
| `results[].deletedAt` | object |  |
| `results[].deletedBy` | object |  |
| `results[].document` | string |  |
| `results[].einvoice` | boolean |  |
| `results[].email` | string |  |
| `results[].emailThread` | string |  |
| `results[].exportedAt` | object |  |
| `results[].exportedBy` | object |  |
| `results[].exportFailedAt` | object |  |
| `results[].hasEmailThreadWithNewReplies` | boolean |  |
| `results[].hasEmailThreadWithReplies` | boolean |  |
| `results[].id` | number |  |
| `results[].modifiedAt` | object |  |
| `results[].modifiedBy` | object |  |
| `results[].modifier` | object |  |
| `results[].organization` | string |  |
| `results[].pages[]` | string |  |
| `results[].prediction.source` | string |  |
| `results[].prediction.version` | object |  |
| `results[].purgedAt` | object |  |
| `results[].purgedBy` | object |  |
| `results[].queue` | string |  |
| `results[].rejectedAt` | object |  |
| `results[].rejectedBy` | object |  |
| `results[].relatedEmails[]` | string |  |
| `results[].relations[]` | string |  |
| `results[].restrictedAccess` | boolean |  |
| `results[].rirPollId` | string |  |
| `results[].schema` | string |  |
| `results[].status` | string |  |
| `results[].suggestedEdit` | object |  |
| `results[].timeSpent` | number |  |
| `results[].trainingEnabled` | boolean |  |
| `results[].url` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `POST /annotations/search` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-annotations.md) for the provider-specific parameters and requirements.

