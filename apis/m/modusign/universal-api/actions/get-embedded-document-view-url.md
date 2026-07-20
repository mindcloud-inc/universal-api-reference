# Modusign: Get Embedded Document View URL

Retrieves an embedded document view URL from Modusign.

```
GET https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-embedded-document-view-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-embedded-document-view-url?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-embedded-document-view-url?${params}`, {
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
| `documentId` | string | yes | The Modusign document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "embeddedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `embeddedUrl` | string | The embedded document view URL. |

## Native endpoint

Through the native Modusign API, this operation is `GET /documents/:documentId/embedded-view` (base URL `https://api.modusign.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-embedded-document-view-url.md) for the provider-specific parameters and requirements.

