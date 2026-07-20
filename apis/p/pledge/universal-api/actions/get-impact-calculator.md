# Pledge: Get Impact Calculator

Retrieves an impact calculator from Pledge.

```
GET https://connect.mindcloud.co/v1/universal/pledge/latest/actions/get-impact-calculator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pledge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/get-impact-calculator?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pledge/latest/actions/get-impact-calculator?${params}`, {
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
| `id` | string | yes | Impact calculator ID. |

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

Through the native Pledge API, this operation is `GET /impact_calculators/[:id]` (base URL `https://api.pledge.to/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-impact-calculator.md) for the provider-specific parameters and requirements.

