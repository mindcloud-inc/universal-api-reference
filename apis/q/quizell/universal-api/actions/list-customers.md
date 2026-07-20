# Quizell: List Customers

Finds customers in Quizell with search and pagination.

```
GET https://connect.mindcloud.co/v1/universal/quizell/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quizell `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quizell/latest/actions/list-customers?${params}`, {
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
| `search` | string | no | Search term to filter customers by name, email, etc. |

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

Through the native Quizell API, this operation is `GET /customers/list` (base URL `https://api.quizell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

