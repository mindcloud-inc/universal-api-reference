# Skribble Sign: Get Document Page Preview

Retrieves a document page preview from Skribble Sign.

```
GET https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-document-page-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-document-page-preview?connectionId=$CONNECTION_ID&documentId=string&pageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "pageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-document-page-preview?${params}`, {
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
| `documentId` | string | yes | The document ID. |
| `pageId` | number | yes | The document page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Preview image bytes when ready. |
| `type` | string | Raw response wrapper type. |

## Native endpoint

Through the native Skribble Sign API, this operation is `GET /v2/documents/:documentId/pages/:pageId` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-page-preview.md) for the provider-specific parameters and requirements.

