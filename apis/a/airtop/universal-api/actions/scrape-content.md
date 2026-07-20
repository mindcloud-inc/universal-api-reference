# Airtop: Scrape Content

Scrapes content from an Airtop window.

```
GET https://connect.mindcloud.co/v1/universal/airtop/latest/actions/scrape-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airtop/latest/actions/scrape-content?connectionId=$CONNECTION_ID&sessionId=string&windowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string",
  "windowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airtop/latest/actions/scrape-content?${params}`, {
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
| `sessionId` | string | yes |  |
| `windowId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airtop API returns.

## Native endpoint

Through the native Airtop API, this operation is `POST /sessions/:sessionId/windows/:windowId/scrape-content` (base URL `https://api.airtop.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-content.md) for the provider-specific parameters and requirements.

