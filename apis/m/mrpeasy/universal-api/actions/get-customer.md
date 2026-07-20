# MRPeasy: Get Customer

Retrieves a customer from MRPeasy.

```
GET https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MRPeasy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/get-customer?${params}`, {
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
| `customerId` | number | yes | MRPeasy customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "contactData": [
        "string"
      ],
      "created": "string",
      "customerId": 1,
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `contactData` | array |  |
| `created` | string |  |
| `customerId` | number |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native MRPeasy API, this operation is `GET /customers/{{customerId}}` (base URL `https://api.mrpeasy.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

