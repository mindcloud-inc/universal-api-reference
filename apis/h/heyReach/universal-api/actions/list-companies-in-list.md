# Hey Reach: List Companies In List

Retrieves companies from a Hey Reach list.

```
GET https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-companies-in-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-companies-in-list?connectionId=$CONNECTION_ID&limit=25&offset=0&listId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "listId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-companies-in-list?${params}`, {
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
| `listId` | number | yes |  |
| `offset` | number | no |  |
| `keyword` | string | no |  |
| `limit` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "totalCount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `totalCount` | string |  |

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/list/GetCompaniesFromList` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies-in-list.md) for the provider-specific parameters and requirements.

