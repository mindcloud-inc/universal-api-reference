# Pledge: Update Impact Calculator

Updates an impact calculator in Pledge.

```
PUT https://connect.mindcloud.co/v1/universal/pledge/latest/actions/update-impact-calculator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pledge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/update-impact-calculator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pledge/latest/actions/update-impact-calculator', {
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
| `id` | string | yes | Impact calculator ID. |
| `name` | string | no | Impact calculator name. |
| `icon` | string | no | Impact calculator icon. |
| `color` | string | no | Primary hex color. |
| `formula` | string | no | Formula used to compute tracked amount or impact. |
| `description` | string | no | Text displayed after the amount. |
| `organizationIds[]` | array<string> | no | Organizations to scope the calculator to. |
| `externalId` | string | no | Fundraiser ID to scope the calculator to. |
| `currencySymbol` | string | no | Currency symbol to display. |
| `info` | string | no | Additional information shown on the back of the calculator. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "color": "string",
      "createdAt": "string",
      "currencySymbol": "string",
      "description": "string",
      "formula": "string",
      "icon": "string",
      "id": "string",
      "info": "string",
      "name": "Ava Chen",
      "style": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `color` | string |  |
| `createdAt` | string |  |
| `currencySymbol` | string |  |
| `description` | string |  |
| `formula` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `info` | string |  |
| `name` | string |  |
| `style` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Pledge API, this operation is `PATCH /impact_calculators/[:id]` (base URL `https://api.pledge.to/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-impact-calculator.md) for the provider-specific parameters and requirements.

