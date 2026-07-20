# CoordinateHQ: Add Organization Stakeholder



```
POST https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/add-organization-stakeholder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoordinateHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/add-organization-stakeholder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/add-organization-stakeholder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes |  |
| `stakeholderEmailAddress` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entityType": "string",
      "externalObjectId": {},
      "lastModifiedDt": "string",
      "stakeholderEmailAddress": "ava@example.com",
      "stakeholderFullName": {},
      "stakeholderId": "string",
      "stakeholderPhone": {},
      "stakeholderProjectId": "string",
      "stakeholderRelatedOrgId": "string",
      "stakeholderTitle": {},
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entityType` | string |  |
| `externalObjectId` | object |  |
| `lastModifiedDt` | string |  |
| `stakeholderEmailAddress` | string |  |
| `stakeholderFullName` | object |  |
| `stakeholderId` | string |  |
| `stakeholderPhone` | object |  |
| `stakeholderProjectId` | string |  |
| `stakeholderRelatedOrgId` | string |  |
| `stakeholderTitle` | object |  |
| `vendorId` | string |  |

## Native endpoint

Through the native CoordinateHQ API, this operation is `POST /organizations/:organizationId/stakeholders` (base URL `https://app.coordinatehq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-organization-stakeholder.md) for the provider-specific parameters and requirements.

