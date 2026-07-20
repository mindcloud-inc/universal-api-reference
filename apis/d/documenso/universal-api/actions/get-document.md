# Documenso: Get Document

Retrieves a document from Documenso.

```
GET https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenso `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-document?connectionId=$CONNECTION_ID&envelopeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "envelopeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-document?${params}`, {
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
| `envelopeId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "internalVersion": 1,
      "recipients": [
        {}
      ],
      "secondaryId": "string",
      "source": "string",
      "status": "string",
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `externalId` | string |  |
| `fields` | array<object> |  |
| `id` | string |  |
| `internalVersion` | number |  |
| `recipients` | array<object> |  |
| `secondaryId` | string |  |
| `source` | string |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `visibility` | string |  |

## Native endpoint

Through the native Documenso API, this operation is `GET /envelope/:envelopeId` (base URL `https://app.documenso.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

