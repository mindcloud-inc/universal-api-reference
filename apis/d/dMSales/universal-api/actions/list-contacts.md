# DMSales: List Contacts

Retrieves contacts from DMSales.

```
GET https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMSales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/list-contacts?${params}`, {
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
| `paidLeads` | string | no | Whether to display paid leads: true, false, or all. One of: `0`, `1`, `2`. Default: `all`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "all": 1,
      "data": [
        {}
      ],
      "limit": 1,
      "page": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `all` | number |  |
| `data` | array<object> |  |
| `limit` | number |  |
| `page` | number |  |
| `total` | number |  |

## Native endpoint

Through the native DMSales API, this operation is `GET /api/persons/list` (base URL `https://app.dmsales.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

