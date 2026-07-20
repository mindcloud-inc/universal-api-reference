# Retently: List Companies

Retrieves a list of companies from Retently.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-companies?${params}`, {
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
| `page` | number | no | The current page number. Default 1; Default: `1`. |
| `limit` | number | no | The items limit. Default 20. Maximum 1,000; Default: `20`. |
| `sort` | string | no | Use â-â to pull results in descending order. Example: sort=-companyName |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "contactsCount": 1,
      "createdDate": "string",
      "cxMetrics": {},
      "domain": "string",
      "id": "string",
      "industryName": "Ava Chen",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `contactsCount` | number |  |
| `createdDate` | string |  |
| `cxMetrics` | object |  |
| `domain` | string |  |
| `id` | string |  |
| `industryName` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Retently API, this operation is `GET /api/v2/companies` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

