# UniOne: Get Webhook

Retrieves a webhook from UniOne by URL.

```
GET https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-webhook?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Funione-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/unione-webhook"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-webhook?${params}`, {
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
| `url` | string | yes | Webhook URL to look up. Example: `https://example.com/unione-webhook`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UniOne API returns.

## Native endpoint

Through the native UniOne API, this operation is `POST webhook/get.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

