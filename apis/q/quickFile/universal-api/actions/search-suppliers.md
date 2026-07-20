# QuickFile: Search Suppliers



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-suppliers?connectionId=$CONNECTION_ID&limit=25&offset=0&sortBy=CompanyName&sortDirection=ASC" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "limit": "25",
  "offset": "0",
  "sortBy": "CompanyName",
  "sortDirection": "ASC"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-suppliers?${params}`, {
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
| `companyName` | string | no | Whole or partial supplier company name |
| `contactName` | string | no | Whole or partial supplier contact name |
| `email` | string | no | Whole or partial supplier email address |
| `limit` | number | yes | Maximum number of suppliers to return Default: `25`. |
| `offset` | number | yes | Page offset for supplier results Default: `0`. |
| `sortBy` | string | yes | Field used to order supplier results Default: `CompanyName`. |
| `sortDirection` | string | yes | Direction used to order supplier results Default: `ASC`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "contactName": "Ava Chen",
      "currency": "string",
      "email": "ava@example.com",
      "isArchived": true,
      "supplierId": 1,
      "telephone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string | Supplier company name. |
| `contactName` | string | Primary supplier contact name. |
| `currency` | string | Supplier currency. |
| `email` | string | Primary supplier email address. |
| `isArchived` | boolean | Whether the supplier is archived. |
| `supplierId` | number | QuickFile supplier identifier. |
| `telephone` | string | Primary supplier telephone number. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /supplier/search` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-suppliers.md) for the provider-specific parameters and requirements.

