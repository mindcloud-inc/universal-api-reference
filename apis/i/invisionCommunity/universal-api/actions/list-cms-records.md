# Invision Community: List CMS Records



```
GET https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/list-cms-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invision Community `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/list-cms-records?connectionId=$CONNECTION_ID&limit=25&offset=0&database_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "database_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/list-cms-records?${params}`, {
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
| `database_id` | number | yes | Database identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "id": 1,
      "page": 1,
      "perPage": 1,
      "results": [
        {}
      ],
      "title": "string",
      "totalPages": 1,
      "totalResults": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `id` | number |  |
| `page` | number |  |
| `perPage` | number |  |
| `results` | array<object> |  |
| `title` | string |  |
| `totalPages` | number |  |
| `totalResults` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Invision Community API, this operation is `GET /cms/records/:database_id` (base URL `{{credentials.communityBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cms-records.md) for the provider-specific parameters and requirements.

