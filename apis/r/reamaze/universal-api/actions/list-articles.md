# Reamaze: List Articles



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-articles?${params}`, {
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
| `status` | string | no | `status` with `published`, `draft`, or `internal` will show only Published, Draft, or Internal articles respectively. |
| `published` | string | no | `status` with `published`, `draft`, or `internal` will show only Published, Draft, or Internal articles respectively. |
| `draft` | string | no | `status` with `published`, `draft`, or `internal` will show only Published, Draft, or Internal articles respectively. |
| `internal` | string | no | `status` with `published`, `draft`, or `internal` will show only Published, Draft, or Internal articles respectively. |
| `q` | string | no | `q` with any string will search over articles by keywords. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articles": [
        {}
      ],
      "pageCount": 1,
      "pageSize": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articles` | array<object> |  |
| `pageCount` | number |  |
| `pageSize` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /articles` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-articles.md) for the provider-specific parameters and requirements.

