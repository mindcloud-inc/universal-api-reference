# Diffbot: Extract With Custom API

Extracts a page with a named Diffbot Custom API.

```
GET https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/extract-with-custom-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/extract-with-custom-api?connectionId=$CONNECTION_ID&customApiName=Ava%20Chen&pageUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customApiName": "Ava Chen",
  "pageUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/extract-with-custom-api?${params}`, {
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
| `customApiName` | string | yes | Custom API name to execute. |
| `pageUrl` | string | yes | Page URL to process with a named Custom API. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Diffbot API returns.

## Native endpoint

Through the native Diffbot API, this operation is `GET /v3/custom` (base URL `https://api.diffbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-with-custom-api.md) for the provider-specific parameters and requirements.

