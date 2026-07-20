# Dubble: Get Guide as Markdown

Retrieves a guide as Markdown from Dubble.

```
GET https://connect.mindcloud.co/v1/universal/dubble/latest/actions/get-guide-as-markdown
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dubble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubble/latest/actions/get-guide-as-markdown?connectionId=$CONNECTION_ID&guideId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guideId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dubble/latest/actions/get-guide-as-markdown?${params}`, {
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
| `guideId` | string | yes | The ID of the guide |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dubble API returns.

## Native endpoint

Through the native Dubble API, this operation is `GET /guides/:guideId/markdown` (base URL `https://api.dubble.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-guide-as-markdown.md) for the provider-specific parameters and requirements.

