# Skribble: Get Document Page Preview

Retrieves a preview image for a document page in Skribble.

```
GET https://connect.mindcloud.co/v1/universal/skribble/latest/actions/get-document-page-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/get-document-page-preview?connectionId=$CONNECTION_ID&documentId=string&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribble/latest/actions/get-document-page-preview?${params}`, {
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
| `documentId` | string | yes | The Skribble document ID. |
| `pageId` | string | yes | The page index starting at 0. |
| `scale` | number | no | Preview scale percentage, such as 20 or 100. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skribble API returns.

## Native endpoint

Through the native Skribble API, this operation is `GET /v2/documents/:documentId/pages/:pageId` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-page-preview.md) for the provider-specific parameters and requirements.

