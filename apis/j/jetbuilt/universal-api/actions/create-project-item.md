# Jetbuilt: Create Project Item



```
POST https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-project-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-project-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-project-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currencyCode` | string | no |  |
| `externalNotes` | string | no |  |
| `manufacturerName` | string | no |  |
| `metadata` | object | no |  |
| `notes` | string | no |  |
| `price` | number | no |  |
| `quantityPerRoom` | number | no |  |
| `roomName` | string | no |  |
| `shippingCost` | number | no |  |
| `shippingPrice` | number | no |  |
| `shortDescription` | string | no |  |
| `systemName` | string | no |  |
| `taxEquipment` | boolean | no |  |
| `taxShipping` | boolean | no |  |
| `projectId` | string | yes |  |
| `model` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jetbuilt API returns.

## Native endpoint

Through the native Jetbuilt API, this operation is `POST projects/:projectId/items` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-item.md) for the provider-specific parameters and requirements.

