# Camio: Search Cameras

Finds cameras in Camio by search text.

```
GET https://connect.mindcloud.co/v1/universal/camio/latest/actions/search-cameras
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/camio/latest/actions/search-cameras?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/camio/latest/actions/search-cameras?${params}`, {
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
| `text` | string | no | Optional text that narrows camera search results. |

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
| `query` | object | The parsed Camio camera search query. |
| `result` | object | The camera-search result envelope. |

## Native endpoint

Through the native Camio API, this operation is `GET /search/cameras` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-cameras.md) for the provider-specific parameters and requirements.

