# Simpro: List Customers



```
GET https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-customers?connectionId=$CONNECTION_ID&companyId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-customers?${params}`, {
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
| `companyId` | number | yes | Simpro company ID. Single-company builds usually use 0. Default: `0`. Example: `0`. |
| `columns[]` | array<string> | no | Columns to return for each customer. Example: `ID,CompanyName,Email`. |
| `pageSize` | number | no | Maximum customers per page. Default: `50`. Example: `50`. |
| `page` | number | no | Page number. Default: `1`. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderby[]` | array<string> | no | Sort columns, prefix with - for descending. Example: `-ID`. |
| `limit` | number | no | Hard limit for number of results. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "familyName": "Ava Chen",
      "givenName": "Ava Chen",
      "Href": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `familyName` | string |  |
| `givenName` | string |  |
| `Href` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Simpro API, this operation is `GET /companies/:companyId/customers/` (base URL `https://mindcloud.simprosuite.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

