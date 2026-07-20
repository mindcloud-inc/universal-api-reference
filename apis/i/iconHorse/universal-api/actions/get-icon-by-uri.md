# Icon Horse: Get Icon by URI

Retrieves a website icon from Icon Horse by URI.

```
GET https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon-by-uri
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Icon Horse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon-by-uri?connectionId=$CONNECTION_ID&uri=https%253A%252F%252Fwikipedia.org" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uri": "https%3A%2F%2Fwikipedia.org"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon-by-uri?${params}`, {
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
| `uri` | string | yes | URL-encoded full URI to resolve into an icon, such as https%3A%2F%2Fwikipedia.org. Default: `https%3A%2F%2Fwikipedia.org`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Icon Horse API returns.

## Native endpoint

Through the native Icon Horse API, this operation is `GET /icon/:uri` (base URL `https://icon.horse`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-icon-by-uri.md) for the provider-specific parameters and requirements.

