# Mendeley: List Trashed Documents



```
GET https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/list-trashed-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/list-trashed-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/list-trashed-documents?${params}`, {
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
| `deletedSince` | string | no | Return only documents deleted since this ISO 8601 timestamp. |
| `groupId` | string | no | Return trashed documents for the specified group. |
| `modifiedSince` | string | no | Return only documents modified since this ISO 8601 timestamp. |
| `order` | string | no | Sort order. |
| `sort` | string | no | Field to sort on. |
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

Through the native Mendeley API, this operation is `GET /trash` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-trashed-documents.md) for the provider-specific parameters and requirements.

