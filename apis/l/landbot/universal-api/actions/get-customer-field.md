# Landbot: Get Customer Field

Retrieves a customer field from Landbot.

```
GET https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-customer-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-customer-field?connectionId=$CONNECTION_ID&customerId=1&fieldName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "fieldName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-customer-field?${params}`, {
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
| `customerId` | number | yes | Customer ID that owns the field. |
| `fieldName` | string | yes | Field name to retrieve from the customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `type` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Landbot API, this operation is `GET /v1/customers/:customer_id/fields/:field_name/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-field.md) for the provider-specific parameters and requirements.

