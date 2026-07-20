# Fleetio: Update Issue

Updates an existing issue in Fleetio.

```
PUT https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-issue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the relevant record |
| `assetId` | number | no | The ID of the asset associated with the Issue. |
| `assetType` | string | no | The type of the asset associated with the Issue. |
| `summary` | string | no | A short summary of the Issue. |
| `description` | string | no | A longer description of the Issue. |
| `reportedById` | number | no | The id of the `Contact` who reported this Issue. |
| `reportedAt` | date | no | The date and time this Issue is reported. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `issuePriorityId` | number | no | The id of the associated `IssuePriority` for this Issue. |
| `number` | number | no | A unique identifier for the Issue. |
| `dueDate` | date | no | The date on which this Issue should be resolved by. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `dueMeterValue` | number | no | The meter value at which this Issue should be resolved by. |
| `dueSecondaryMeterValue` | number | no | The secondary meter value at which this Issue should be resolved by. |
| `faultId` | number | no | The id of the `Fault` associated with this Issue. |
| `customFields` | object | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
| `meterEntryAttributes` | object | no | An Issue may be associated with a [Meter Entry](/docs/api/meter-entries). |
| `secondaryMeterEntryAttributes` | object | no | An Issue may be associated with a secondary [Meter Entry](/docs/api/meter-entries). |
| `commentsAttributes` | array<object> | no |  |
| `documentsAttributes` | array<object> | no | An array of one or more document objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |
| `imagesAttributes` | array<object> | no | An array of one or more image objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |
| `assignedContactIds` | array<number> | no | An array of ids of assigned `Contacts` related to the Issue. |
| `labelIds` | array<number> | no |  |

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
      "attachmentPermissions": {},
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
| `attachmentPermissions` | object |  |
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

Through the native Fleetio API, this operation is `PATCH issues/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-issue.md) for the provider-specific parameters and requirements.

