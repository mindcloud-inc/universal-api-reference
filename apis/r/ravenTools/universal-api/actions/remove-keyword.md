# Raven Tools: Remove Keyword

Deletes a keyword from a domain in Raven Tools.

```
DELETE https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/remove-keyword
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/remove-keyword?connectionId=$CONNECTION_ID&domain=mindcloud.co&keyword=seo%20automation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "mindcloud.co",
  "keyword": "seo automation"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/remove-keyword?${params}`, {
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
| `domain` | string | yes | The domain to remove the keyword from. Default: `codex-raven-tools-temp.example`. Example: `mindcloud.co`. |
| `keyword` | string | yes | The keyword to remove. Default: `codex raven default test keyword`. Example: `seo automation`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Provider result message. |

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-keyword.md) for the provider-specific parameters and requirements.

