# Fleetio: Retrieve Issue

Retrieves a specific issue from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-issue?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-issue?${params}`, {
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
| `id` | string | yes | The id of the relevant record |
| `includes` | string | no | A comma-separated list of additional attributes to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asset": {
        "id": 1
      },
      "assetType": "string",
      "closedAt": {},
      "closedBy": {},
      "closedNote": "string",
      "commentsCount": 1,
      "createdAt": "string",
      "creationType": "string",
      "description": "string",
      "documentsCount": 1,
      "dueDate": {},
      "dueMeterValue": {},
      "dueSecondaryMeterValue": {},
      "fault": {},
      "id": 1,
      "imagesCount": 1,
      "isOverdue": true,
      "issuePriority": {
        "alias": {},
        "default": true,
        "description": "string",
        "enabled": true,
        "id": 1,
        "name": "Ava Chen",
        "position": 1,
        "slug": "string"
      },
      "isWatched": true,
      "number": 1,
      "reportedAt": "string",
      "reportedBy": {
        "id": 1
      },
      "resolvable": {},
      "resolvableType": {},
      "resolvedAt": {},
      "resolvedBy": {},
      "resolvedNote": "string",
      "state": "string",
      "submittedInspectionForm": {
        "id": 1
      },
      "summary": "string",
      "updatedAt": "string",
      "watchersCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asset.id` | number |  |
| `assetType` | string |  |
| `closedAt` | object |  |
| `closedBy` | object |  |
| `closedNote` | string |  |
| `commentsCount` | number |  |
| `createdAt` | string |  |
| `creationType` | string |  |
| `description` | string |  |
| `documentsCount` | number |  |
| `dueDate` | object |  |
| `dueMeterValue` | object |  |
| `dueSecondaryMeterValue` | object |  |
| `fault` | object |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `isOverdue` | boolean |  |
| `issuePriority.alias` | object |  |
| `issuePriority.default` | boolean |  |
| `issuePriority.description` | string |  |
| `issuePriority.enabled` | boolean |  |
| `issuePriority.id` | number |  |
| `issuePriority.name` | string |  |
| `issuePriority.position` | number |  |
| `issuePriority.slug` | string |  |
| `isWatched` | boolean |  |
| `number` | number |  |
| `reportedAt` | string |  |
| `reportedBy.id` | number |  |
| `resolvable` | object |  |
| `resolvableType` | object |  |
| `resolvedAt` | object |  |
| `resolvedBy` | object |  |
| `resolvedNote` | string |  |
| `state` | string |  |
| `submittedInspectionForm.id` | number |  |
| `summary` | string |  |
| `updatedAt` | string |  |
| `watchersCount` | number |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET issues/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-issue.md) for the provider-specific parameters and requirements.

