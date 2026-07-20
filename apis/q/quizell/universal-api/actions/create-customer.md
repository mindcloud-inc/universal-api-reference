# Quizell: Create Customer

Creates a new customer in Quizell.

```
POST https://connect.mindcloud.co/v1/universal/quizell/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quizell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quizell/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerData` | object | yes | Customer data payload. |
| `customerCustomData` | object | no | Optional custom customer fields payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "address2": "string",
      "city": "string",
      "country": "string",
      "custom_fields_data": [
        {}
      ],
      "date": "string",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "lead_id": 1,
      "organisation": "string",
      "phone_number": "string",
      "quiz_id": 1,
      "result_history": "string",
      "state": "string",
      "terms_conditions": true,
      "website": "string",
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `city` | string |  |
| `country` | string |  |
| `custom_fields_data` | array<object> |  |
| `date` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `lead_id` | number |  |
| `organisation` | string |  |
| `phone_number` | string |  |
| `quiz_id` | number |  |
| `result_history` | string |  |
| `state` | string |  |
| `terms_conditions` | boolean |  |
| `website` | string |  |
| `zip_code` | string |  |

## Native endpoint

Through the native Quizell API, this operation is `POST /customers/store` (base URL `https://api.quizell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

