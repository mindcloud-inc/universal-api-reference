# GorillaDesk: Retrieve Customer

Retrieves a customer from GorillaDesk.

```
GET https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/retrieve-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GorillaDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/retrieve-customer?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/retrieve-customer?${params}`, {
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
| `customerId` | string | yes | Customer Id |
| `include[]` | array<string> | no | Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountNumber": "string",
      "company": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "phones": [
        [
          {}
        ]
      ],
      "profileUrl": "https://example.com",
      "state": "string",
      "status": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountNumber` | string |  |
| `company` | string |  |
| `created` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `phones[]` | array<object> |  |
| `phones[].id` | string |  |
| `phones[].phone` | string |  |
| `phones[].type` | string |  |
| `profileUrl` | string |  |
| `state` | string |  |
| `status` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native GorillaDesk API, this operation is `GET /customers/:customerId` (base URL `https://api.gorilladesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-customer.md) for the provider-specific parameters and requirements.

