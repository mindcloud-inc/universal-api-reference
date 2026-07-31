# Bunnies.io: Get Random Bunny Media



```
GET https://connect.mindcloud.co/v1/universal/bunniesio/latest/actions/get-random-bunny-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bunnies.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunniesio/latest/actions/get-random-bunny-media?connectionId=$CONNECTION_ID&media=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "media": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunniesio/latest/actions/get-random-bunny-media?${params}`, {
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
| `media` | list | yes | One requested native media format. The provider redirects to the raw media URL. One of: `0`, `1`, `2`, `3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bunnies.io API returns.

## Native endpoint

Through the native Bunnies.io API, this operation is `GET /v2/loop/random/redirect/` (base URL `https://api.bunnies.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-bunny-media.md) for the provider-specific parameters and requirements.

