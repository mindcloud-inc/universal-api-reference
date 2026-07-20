# NextLead: Create Sale

Creates a new sales deal in NextLead.

```
POST https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/create-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/create-sale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "column": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/create-sale', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "column": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Sale name. |
| `column` | string | yes | Sales column identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "salesDeal": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `salesDeal` | object |  |

## Native endpoint

Through the native NextLead API, this operation is `POST /api/v2/receive/sales/create-sale` (base URL `https://dashboard.nextlead.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sale.md) for the provider-specific parameters and requirements.

