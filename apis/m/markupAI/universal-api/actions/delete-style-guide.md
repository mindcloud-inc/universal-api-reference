# Markup AI: Delete Style Guide

Deletes an existing style guide from Markup AI.

```
DELETE https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/delete-style-guide
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/delete-style-guide?connectionId=$CONNECTION_ID&styleGuideId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "styleGuideId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/delete-style-guide?${params}`, {
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
| `styleGuideId` | string | yes | UUID of the style guide to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Markup AI API returns.

## Native endpoint

Through the native Markup AI API, this operation is `DELETE /v1/style-guides/:style_guide_id` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-style-guide.md) for the provider-specific parameters and requirements.

