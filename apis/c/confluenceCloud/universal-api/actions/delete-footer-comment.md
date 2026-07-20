# Confluence: Delete Footer Comment

Deletes an existing footer comment from Confluence.

```
DELETE https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/delete-footer-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/delete-footer-comment?connectionId=$CONNECTION_ID&cloudId=string&commentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "commentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/delete-footer-comment?${params}`, {
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
| `cloudId` | string | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `commentId` | string | yes | ID of the footer comment. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Confluence API returns.

## Native endpoint

Through the native Confluence API, this operation is `DELETE /ex/confluence/:cloudId/wiki/api/v2/footer-comments/:commentId` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-footer-comment.md) for the provider-specific parameters and requirements.

