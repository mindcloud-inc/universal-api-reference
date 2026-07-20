# CoordinateHQ: List Projects



```
GET https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoordinateHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-projects?${params}`, {
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
| `lastModifiedDt` | string | no |  |
| `sort` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": [
        {
          "customerId": "string",
          "customerName": "Ava Chen"
        }
      ],
      "customFields": {
        "jurisdiction": "string",
        "scopeOfWork": "string"
      },
      "entityType": "string",
      "entityUrl": "https://example.com",
      "externalObjectId": {},
      "lastModifiedDt": "string",
      "projectActive": true,
      "projectDescription": {},
      "projectEstimatedEffort": {},
      "projectEstimatedEndDate": {},
      "projectEstimatedStartDate": {},
      "projectId": "string",
      "projectManagerEmail": "ava@example.com",
      "projectManagerFullName": "Ava Chen",
      "projectName": "Ava Chen",
      "projectStatus": "string",
      "projectSummary": {},
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers[].customerId` | string |  |
| `customers[].customerName` | string |  |
| `customFields.jurisdiction` | string |  |
| `customFields.scopeOfWork` | string |  |
| `entityType` | string |  |
| `entityUrl` | string |  |
| `externalObjectId` | object |  |
| `lastModifiedDt` | string |  |
| `projectActive` | boolean |  |
| `projectDescription` | object |  |
| `projectEstimatedEffort` | object |  |
| `projectEstimatedEndDate` | object |  |
| `projectEstimatedStartDate` | object |  |
| `projectId` | string |  |
| `projectManagerEmail` | string |  |
| `projectManagerFullName` | string |  |
| `projectName` | string |  |
| `projectStatus` | string |  |
| `projectSummary` | object |  |
| `vendorId` | string |  |

## Native endpoint

Through the native CoordinateHQ API, this operation is `GET /projects` (base URL `https://app.coordinatehq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

