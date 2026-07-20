# Microsoft 365 Excel: Calculate Workbook

Calculates formulas in a Microsoft 365 Excel workbook.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/calculate-workbook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/calculate-workbook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveItemId": "string",
  "calculationType": "Recalculate"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/calculate-workbook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveItemId": "string",
    "calculationType": "Recalculate"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveItemId` | string | yes |  |
| `calculationType` | string | yes | Default: `Recalculate`. Example: `Recalculate`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 Excel API returns.

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/application/calculate` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-workbook.md) for the provider-specific parameters and requirements.

