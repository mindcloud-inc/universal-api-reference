# Zoho CRM: List Leads

Retrieves lead records from Zoho CRM.

```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/list-leads?connectionId=$CONNECTION_ID&limit=25&offset=0&fields=id%2CCompany%2CFull_Name%2CEmail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "fields": "id,Company,Full_Name,Email"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/list-leads?${params}`, {
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
| `fields` | string | yes | Comma-separated lead field API names to return. Accepts multiple values in one string, delimited by `,`. Default: `id,Company,Full_Name,Email`. Example: `id,Company,Full_Name,Email`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids` | string | no | Comma-separated lead record IDs to retrieve. Accepts multiple values in one string, delimited by `,`. Example: `7323083000000731830,7323083000000731831`. |
| `converted` | list<string> | no | Whether to return converted, non-converted, or both lead records. One of: `both`, `false`, `true`. Default: `false`. |
| `cvid` | string | no | Custom view ID to fetch leads from a saved view. Example: `4150868000001944196`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `fullName` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Zoho CRM API, this operation is `GET /Leads` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

