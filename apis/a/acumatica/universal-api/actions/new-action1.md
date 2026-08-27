# Acumatica: Create Project



```
POST https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/new-action1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/new-action1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/new-action1', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingAndAllocationSettings.billingPeriod.value` | string | no |  |
| `billingAndAllocationSettings.billingRule` | object | no |  |
| `billingAndAllocationSettings.billingRule.value` | string | no |  |
| `customer.value` | string | no |  |
| `description.value` | string | no |  |
| `ownerId.value` | string | no |  |
| `projectId.value` | string | no |  |
| `projectTemplateId.value` | string | no |  |
| `status.value` | string | no |  |
| `webServiceEndpoint` | string | no |  |
| `billingAndAllocationSettings.billingPeriod` | object | no |  |
| `endpointVersion` | string | no |  |
| `projectId` | object | yes |  |
| `projectTemplateId` | object | no |  |
| `customer` | object | no |  |
| `billingAndAllocationSettings` | object | no |  |
| `description` | object | no |  |
| `ownerId` | object | no |  |
| `status` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumatica API returns.

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/:webServiceEndpoint/:endpointVersion/Project` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/new-action1.md) for the provider-specific parameters and requirements.

