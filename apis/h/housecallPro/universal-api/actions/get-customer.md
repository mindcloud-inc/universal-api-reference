# Housecall Pro: Get Customer



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=cus_ccdcb54ddb5a42bea9466d386a637af8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "cus_ccdcb54ddb5a42bea9466d386a637af8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-customer?${params}`, {
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
| `customerId` | string | yes | ID of the customer to retrieve. Example: `cus_ccdcb54ddb5a42bea9466d386a637af8`. |
| `expand[]` | array<string> | no | Fields to expand in the response body. Accepts multiple values as an array. Example: `attachments`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "company": "string",
      "companyId": "string",
      "companyName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "homeNumber": "string",
      "id": "string",
      "lastName": "Chen",
      "leadSource": "string",
      "mobileNumber": "string",
      "notes": "string",
      "notificationsEnabled": true,
      "tags": [
        "string"
      ],
      "updatedAt": "string",
      "workNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `company` | string |  |
| `companyId` | string |  |
| `companyName` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `homeNumber` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `leadSource` | string |  |
| `mobileNumber` | string |  |
| `notes` | string |  |
| `notificationsEnabled` | boolean |  |
| `tags` | array<string> |  |
| `updatedAt` | string |  |
| `workNumber` | string |  |

## Native endpoint

Through the native Housecall Pro API, this operation is `GET /customers/:customer_id` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

