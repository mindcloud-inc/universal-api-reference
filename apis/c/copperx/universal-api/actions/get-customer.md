# Copperx: Get Customer

Retrieves customer record details from Copperx.

```
GET https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-customer?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-customer?${params}`, {
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
| `id` | string | yes | Customer ID path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "customerNumber": "string",
      "customerReferenceId": "string",
      "email": "ava@example.com",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "organizationName": "Ava Chen",
      "phone": "string",
      "taxIds": {},
      "updatedAt": "string",
      "visibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `customerNumber` | string |  |
| `customerReferenceId` | string |  |
| `email` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `organizationName` | string |  |
| `phone` | string |  |
| `taxIds` | object |  |
| `updatedAt` | string |  |
| `visibility` | number |  |

## Native endpoint

Through the native Copperx API, this operation is `GET /customers/{id}` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

