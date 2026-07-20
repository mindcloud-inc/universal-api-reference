# Invoiless: Get Customer

Retrieves a customer from Invoiless.

```
GET https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoiless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/get-customer?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/get-customer?${params}`, {
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
| `id` | string | yes | Customer id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__v": 1,
      "_id": "string",
      "attachPdf": true,
      "billTo": {
        "company": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "shortName": "Ava Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "notes": "string",
      "property": "string",
      "shipTo": {
        "company": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "shortName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__v` | number |  |
| `_id` | string |  |
| `attachPdf` | boolean |  |
| `billTo.company` | string |  |
| `billTo.email` | string |  |
| `billTo.name` | string |  |
| `billTo.shortName` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `notes` | string |  |
| `property` | string |  |
| `shipTo.company` | string |  |
| `shipTo.email` | string |  |
| `shipTo.name` | string |  |
| `shipTo.shortName` | string |  |

## Native endpoint

Through the native Invoiless API, this operation is `GET /customers/:id` (base URL `https://api.invoiless.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

