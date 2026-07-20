# Digistore24: List Products

Retrieves a list of products from Digistore24.

```
GET https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-products?${params}`, {
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
| `sortBy` | string | no | Sort products by name or product group |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "language": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "note": "string",
      "productGroupId": 1,
      "productGroupName": "Ava Chen",
      "tag": "string",
      "unitsLeft": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp |
| `id` | number | Product ID |
| `language` | string | Product language |
| `modifiedAt` | date | Last modification timestamp |
| `name` | string | Product name |
| `note` | string | Product note |
| `productGroupId` | number | Product group ID |
| `productGroupName` | string | Product group name |
| `tag` | string | Product tag |
| `unitsLeft` | string | Remaining units or infinite |

## Native endpoint

Through the native Digistore24 API, this operation is `GET /listProducts` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

