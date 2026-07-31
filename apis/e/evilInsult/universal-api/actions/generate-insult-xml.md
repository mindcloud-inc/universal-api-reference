# Evil Insult: Generate Insult (XML)



```
GET https://connect.mindcloud.co/v1/universal/evilInsult/latest/actions/generate-insult-xml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evil Insult `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evilInsult/latest/actions/generate-insult-xml?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evilInsult/latest/actions/generate-insult-xml?${params}`, {
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
| `language` | list | no | Language for the intentionally insulting/offensive provider output. Defaults to English when omitted. One of: `cn`, `de`, `el`, `en`, `es`, `fr`, `ru`, `sw`. Default: `en`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Evil Insult API returns.

## Native endpoint

Through the native Evil Insult API, this operation is `GET /generate_insult.php` (base URL `https://evilinsult.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-insult-xml.md) for the provider-specific parameters and requirements.

