# D-Tools SI: Update Project



```
POST https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D-Tools SI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/update-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectItemsInfosToDelete[].model` | string | no |  |
| `projectItemsInfosToDelete[].quantity` | number | no |  |
| `updateProjectItems[].quantity` | number | no |  |
| `updateProjectItems[].unitCost` | number | no |  |
| `updateProjectItems[].unitPrice` | string | no |  |
| `billingAddress.street1` | string | no |  |
| `newProjectItems[].id` | string | no |  |
| `projectId` | string | no |  |
| `projectItemsInfosToDelete[].manufacturer` | string | no |  |
| `siteAddress.street1` | string | no |  |
| `updateFields[].projectFieldId` | string | no |  |
| `updateProjectItems[].componentId` | string | no |  |
| `billingAddress.street2` | string | no |  |
| `newProjectItems[]` | array<object> | no |  |
| `newProjectItems[].typeId` | string | no |  |
| `siteAddress.street2` | string | no |  |
| `updateFields[].value` | string | no |  |
| `billingAddress.city` | string | no |  |
| `newProjectItems[].componentId` | string | no |  |
| `siteAddress.city` | string | no |  |
| `updateProjectItems[]` | array | no |  |
| `billingAddress.state` | string | no |  |
| `newProjectItems[].manufacturer` | string | no |  |
| `projectItemsInfosToDelete[]` | array | no |  |
| `siteAddress.state` | string | no |  |
| `billingAddress.postalCode` | string | no |  |
| `newProjectItems[].model` | string | no |  |
| `siteAddress` | object | no |  |
| `siteAddress.postalCode` | string | no |  |
| `billingAddress` | object | no |  |
| `billingAddress.country` | string | no |  |
| `newProjectItems[].packageName` | string | no |  |
| `siteAddress.country` | string | no |  |
| `billingAddress.phone` | string | no |  |
| `newProjectItems[].unitCost` | number | no |  |
| `siteAddress.phone` | string | no |  |
| `updateFields[]` | array | no |  |
| `billingAddress.fax` | string | no |  |
| `newProjectItems[].unitPrice` | number | no |  |
| `siteAddress.fax` | string | no |  |
| `newProjectItems[].quantity` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native D-Tools SI API returns.

## Native endpoint

Through the native D-Tools SI API, this operation is `POST https://api.d-tools.com/SI/Publish/Projects/Update` (base URL `https://api.d-tools.com/SI/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

