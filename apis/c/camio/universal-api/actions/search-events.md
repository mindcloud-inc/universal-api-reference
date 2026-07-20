# Camio: Search Events

Finds video events in Camio by search text.

```
GET https://connect.mindcloud.co/v1/universal/camio/latest/actions/search-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/camio/latest/actions/search-events?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/camio/latest/actions/search-events?${params}`, {
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
| `text` | string | yes | The Camio search text to run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "query": {},
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `query` | object | The parsed Camio search query. |
| `result` | object | The search result envelope. |

## Native endpoint

Through the native Camio API, this operation is `GET /search` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-events.md) for the provider-specific parameters and requirements.

