# Autom: Search Bing

Finds Bing search results in Autom.

```
GET https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-bing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-bing?connectionId=$CONNECTION_ID&query=MindCloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "MindCloud"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-bing?${params}`, {
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
| `query` | string | yes | The Bing query to run. Example: `MindCloud`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cc` | string | no | Bing market code such as en-US. Example: `en-US`. |
| `page` | number | no | Result page number to request. Example: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Autom API returns.

## Native endpoint

Through the native Autom API, this operation is `GET /v1/bing/search` (base URL `https://api.autom.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-bing.md) for the provider-specific parameters and requirements.

