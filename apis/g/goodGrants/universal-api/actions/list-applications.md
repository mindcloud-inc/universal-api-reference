# Good Grants: List applications

Retrieves applications from Good Grants.

```
GET https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/list-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Good Grants `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/list-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/list-applications?${params}`, {
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
| `form` | string | no | Filter applications by form slug. |
| `page` | number | no | Page number greater than 0. |
| `perPage` | number | no | Results per page, between 1 and 100. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_page": 1,
      "data": [
        {}
      ],
      "first_page_url": "https://example.com",
      "from": 1,
      "last_page": 1,
      "last_page_url": "https://example.com",
      "next_page_url": "https://example.com",
      "path": "string",
      "per_page": 1,
      "prev_page_url": "https://example.com",
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number |  |
| `data` | array<object> |  |
| `first_page_url` | string |  |
| `from` | number |  |
| `last_page` | number |  |
| `last_page_url` | string |  |
| `next_page_url` | string |  |
| `path` | string |  |
| `per_page` | number |  |
| `prev_page_url` | string |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Good Grants API, this operation is `GET application` (base URL `https://api.cr4ce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applications.md) for the provider-specific parameters and requirements.

