# Paycove: Create Deal

Creates a deal in Paycove.

```
POST https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact": {},
  "lineItems[]": [
    {}
  ],
  "name": "Ava Chen",
  "org": {},
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact": {},
    "lineItems[]": [{}],
    "name": "Ava Chen",
    "org": {},
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | object | yes | Contact object. Provide an existing id or name and email to create a new contact. |
| `crmDealId` | string | no | Associated CRM deal id. |
| `lineItems[]` | array<object> | yes | Array of line item objects. |
| `name` | string | yes | Name of the deal. |
| `org` | object | yes | Organization object. Provide an existing id or organization fields. |
| `type` | string | yes | Deal type. Allowed values: invoice or quote. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminUrl": "https://example.com",
      "checkoutUrl": "https://example.com",
      "contactId": 1,
      "crmDealId": "string",
      "currency": "string",
      "dealName": "Ava Chen",
      "id": 1,
      "orgId": 1,
      "po": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminUrl` | string |  |
| `checkoutUrl` | string |  |
| `contactId` | number |  |
| `crmDealId` | string |  |
| `currency` | string |  |
| `dealName` | string |  |
| `id` | number |  |
| `orgId` | number |  |
| `po` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Paycove API, this operation is `POST deals/with-relations` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

