# Customer.io: List Customer Activities

Retrieves activities for a customer in Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-activities?connectionId=$CONNECTION_ID&customerId=user_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "user_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-activities?${params}`, {
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
| `customerId` | string | yes | The ID of the customer you want to inspect. Example: `user_123`. |
| `idType` | list<string> | no | The type of customer identifier supplied in Customer ID. One of: `cio_id`, `email`, `id`. Example: `id`. |
| `limit` | number | no | The maximum number of results you want to retrieve per page. Example: `100`. |
| `type` | string | no | The type of activity you want to search for. Example: `event`. |
| `name` | string | no | For event and attribute_update types, search by event or attribute name. Example: `user_signed_in`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | string | no | The token for the page of results you want to return. Example: `next-page-token`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": "string",
      "customerIdentifiers": {},
      "data": {},
      "deliveryId": "string",
      "deliveryType": "string",
      "id": "string",
      "name": "Ava Chen",
      "timestamp": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | string | The customer identifier associated with the activity. |
| `customerIdentifiers` | object | The customer identifiers returned with the activity. |
| `data` | object | Activity payload details. |
| `deliveryId` | string | The related delivery identifier when present. |
| `deliveryType` | string | The related delivery type when present. |
| `id` | string | The activity identifier. |
| `name` | string | The event or activity name when present. |
| `timestamp` | number | Unix timestamp when the activity occurred. |
| `type` | string | The activity type. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/customers/:customer_id/activities` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-activities.md) for the provider-specific parameters and requirements.

