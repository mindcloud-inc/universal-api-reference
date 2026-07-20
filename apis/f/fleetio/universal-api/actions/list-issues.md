# Fleetio: List Issues

Retrieves a list of issues from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-issues?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-issues?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "assetType": "string",
      "closedAt": {},
      "closedById": {},
      "commentsCount": 1,
      "createdAt": "string",
      "description": "string",
      "documentsCount": 1,
      "dueDate": {},
      "duePrimaryMeterValue": "string",
      "dueSecondaryMeterValue": {},
      "externalId": {},
      "faultId": {},
      "id": 1,
      "imagesCount": 1,
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
      "name": "Ava Chen",
      "number": "string",
      "overdue": true,
      "reopenedAt": {},
      "reopenedById": {},
      "reportedAt": "string",
      "reportedBy": {
        "defaultImageUrl": "https://example.com",
        "email": "ava@example.com",
        "employee": true,
        "employeeNumber": "string",
        "groupId": 1,
        "id": 1,
        "name": "Ava Chen"
      },
      "resolvableId": {},
      "resolvableType": {},
      "resolvedAt": {},
      "resolvedById": {},
      "state": "string",
      "submittedInspectionFormId": {},
      "summary": "string",
      "updatedAt": "string",
      "vehicle": {
        "color": "string",
        "currentJob": {},
        "defaultImageUrlSmall": "https://example.com",
        "id": 1,
        "licensePlate": "string",
        "make": "string",
        "model": "string",
        "name": "Ava Chen",
        "registrationExpirationMonth": 1,
        "registrationState": {},
        "trim": "string",
        "vin": "string",
        "year": 1
      },
      "watchersCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetType` | string |  |
| `closedAt` | object |  |
| `closedById` | object |  |
| `commentsCount` | number |  |
| `createdAt` | string |  |
| `description` | string |  |
| `documentsCount` | number |  |
| `dueDate` | object |  |
| `duePrimaryMeterValue` | string |  |
| `dueSecondaryMeterValue` | object |  |
| `externalId` | object |  |
| `faultId` | object |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `issuePriority.alias` | object |  |
| `issuePriority.default` | boolean |  |
| `issuePriority.description` | string |  |
| `issuePriority.enabled` | boolean |  |
| `issuePriority.id` | number |  |
| `issuePriority.name` | string |  |
| `issuePriority.position` | number |  |
| `issuePriority.slug` | string |  |
| `name` | string |  |
| `number` | string |  |
| `overdue` | boolean |  |
| `reopenedAt` | object |  |
| `reopenedById` | object |  |
| `reportedAt` | string |  |
| `reportedBy.defaultImageUrl` | string |  |
| `reportedBy.email` | string |  |
| `reportedBy.employee` | boolean |  |
| `reportedBy.employeeNumber` | string |  |
| `reportedBy.groupId` | number |  |
| `reportedBy.id` | number |  |
| `reportedBy.name` | string |  |
| `resolvableId` | object |  |
| `resolvableType` | object |  |
| `resolvedAt` | object |  |
| `resolvedById` | object |  |
| `state` | string |  |
| `submittedInspectionFormId` | object |  |
| `summary` | string |  |
| `updatedAt` | string |  |
| `vehicle.color` | string |  |
| `vehicle.currentJob` | object |  |
| `vehicle.defaultImageUrlSmall` | string |  |
| `vehicle.id` | number |  |
| `vehicle.licensePlate` | string |  |
| `vehicle.make` | string |  |
| `vehicle.model` | string |  |
| `vehicle.name` | string |  |
| `vehicle.registrationExpirationMonth` | number |  |
| `vehicle.registrationState` | object |  |
| `vehicle.trim` | string |  |
| `vehicle.vin` | string |  |
| `vehicle.year` | number |  |
| `watchersCount` | number |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET issues` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-issues.md) for the provider-specific parameters and requirements.

