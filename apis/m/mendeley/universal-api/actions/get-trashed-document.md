# Mendeley: Get Trashed Document



```
GET https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/get-trashed-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/get-trashed-document?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/get-trashed-document?${params}`, {
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
| `id` | string | yes | Identifier (UUID) of the trashed document. |
| `view` | string | no | Includes core document fields plus additional fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "profileId": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | When the document was originally created. |
| `id` | string | UUID of the trashed document. |
| `lastModified` | date | When the document was last modified. |
| `profileId` | string | Profile identifier that owns the document. |
| `title` | string | Title of the trashed document. |
| `type` | string | Mendeley document type. |

## Native endpoint

Through the native Mendeley API, this operation is `GET /trash/:id` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trashed-document.md) for the provider-specific parameters and requirements.

