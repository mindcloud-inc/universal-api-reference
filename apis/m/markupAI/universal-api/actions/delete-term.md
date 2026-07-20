# Markup AI: Delete Term

Deletes an existing term from Markup AI.

```
DELETE https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/delete-term
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/delete-term?connectionId=$CONNECTION_ID&termSetId=string&termId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "termSetId": "string",
  "termId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/delete-term?${params}`, {
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
| `termSetId` | string | yes | UUID of the parent term set. |
| `termId` | string | yes | UUID of the term to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Markup AI API returns.

## Native endpoint

Through the native Markup AI API, this operation is `DELETE /v1/terminology/term-sets/:term_set_id/terms/:term_id` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-term.md) for the provider-specific parameters and requirements.

