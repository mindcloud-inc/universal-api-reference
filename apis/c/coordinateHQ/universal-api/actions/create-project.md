# CoordinateHQ: Create Project



```
POST https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoordinateHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "managerEmailAddress": "ava@example.com",
  "projectName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "managerEmailAddress": "ava@example.com",
    "projectName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `managerEmailAddress` | string | yes |  |
| `projectName` | string | yes |  |
| `externalObjectId` | string | no |  |
| `playbookName` | string | no |  |
| `stakeholderEmail` | string | no |  |
| `stakeholderAssignmentList[]` | array | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": {
        "jurisdiction": {},
        "scopeOfWork": {}
      },
      "entityType": "string",
      "entityUrl": "https://example.com",
      "externalObjectId": "string",
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
| `customFields.jurisdiction` | object |  |
| `customFields.scopeOfWork` | object |  |
| `entityType` | string |  |
| `entityUrl` | string |  |
| `externalObjectId` | string |  |
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

Through the native CoordinateHQ API, this operation is `POST /projects` (base URL `https://app.coordinatehq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

