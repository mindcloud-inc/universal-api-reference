# Ahrefs: Get Keyword Volume History



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-keyword-volume-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-keyword-volume-history?connectionId=$CONNECTION_ID&country=string&keyword=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string",
  "keyword": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-keyword-volume-history?${params}`, {
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
| `country` | string | yes | Two-letter ISO 3166-1 alpha-2 country code. |
| `keyword` | string | yes | Comma-separated keywords to show volume history for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ahrefs API returns.

## Native endpoint

Through the native Ahrefs API, this operation is `GET /keywords-explorer/volume-history` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-keyword-volume-history.md) for the provider-specific parameters and requirements.

