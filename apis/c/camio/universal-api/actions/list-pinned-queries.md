# Camio: List Pinned Queries

Retrieves pinned queries from Camio.

```
GET https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-pinned-queries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-pinned-queries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-pinned-queries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "query": {},
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The pinned query id. |
| `query` | object | The parsed Camio query object. |
| `text` | string | The pinned query text. |

## Native endpoint

Through the native Camio API, this operation is `GET /users/:user/queries/pinned` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pinned-queries.md) for the provider-specific parameters and requirements.

