# PayWhirl: Get Customer Profile

Retrieves a customer's profile from PayWhirl.

```
GET https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/get-customer-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/get-customer-profile?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/get-customer-profile?${params}`, {
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
| `customerId` | number | yes | The PayWhirl customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {
          "city": "string",
          "country": "string",
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "state": "string"
        }
      ],
      "answers": [
        {
          "answer": "string",
          "label": "string"
        }
      ],
      "customer": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses[].city` | string |  |
| `addresses[].country` | string |  |
| `addresses[].firstName` | string |  |
| `addresses[].id` | number |  |
| `addresses[].lastName` | string |  |
| `addresses[].state` | string |  |
| `answers[].answer` | string |  |
| `answers[].label` | string |  |
| `customer.email` | string |  |
| `customer.firstName` | string |  |
| `customer.id` | number |  |
| `customer.lastName` | string |  |

## Native endpoint

Through the native PayWhirl API, this operation is `GET /customer/profile/{id}` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-profile.md) for the provider-specific parameters and requirements.

