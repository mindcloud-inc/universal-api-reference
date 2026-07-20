# Pledge: Create Impact Calculator

Creates an impact calculator in Pledge.

```
POST https://connect.mindcloud.co/v1/universal/pledge/latest/actions/create-impact-calculator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pledge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/create-impact-calculator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "icon": "string",
  "color": "string",
  "formula": "string",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pledge/latest/actions/create-impact-calculator', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "icon": "string",
    "color": "string",
    "formula": "string",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Impact calculator name. |
| `icon` | string | yes | Impact calculator icon. |
| `color` | string | yes | Primary hex color. |
| `formula` | string | yes | Formula used to compute tracked amount or impact. |
| `description` | string | yes | Text displayed after the amount. |
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

Through the native Pledge API, this operation is `POST /impact_calculators` (base URL `https://api.pledge.to/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-impact-calculator.md) for the provider-specific parameters and requirements.

