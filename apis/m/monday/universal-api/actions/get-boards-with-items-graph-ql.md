# Monday: Get Boards With items (GraphQL)



```
GET https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-boards-with-items-graph-ql
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monday `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-boards-with-items-graph-ql?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-boards-with-items-graph-ql?${params}`, {
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
| `query` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "id": "string",
      "itemsPage": {
        "items": [
          {
            "id": "string",
            "name": "Ava Chen"
          }
        ]
      },
      "itemTerminology": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `id` | string |  |
| `itemsPage.items[].id` | string |  |
| `itemsPage.items[].name` | string |  |
| `itemTerminology` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Monday API, this operation is `POST` (base URL `https://api.monday.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-boards-with-items-graph-ql.md) for the provider-specific parameters and requirements.

