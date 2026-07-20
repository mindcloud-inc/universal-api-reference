# Documenso: Get Template

Retrieves a template from Documenso.

```
GET https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenso `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-template?${params}`, {
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
| `templateId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "envelopeId": "string",
      "externalId": "string",
      "fields": [
        {}
      ],
      "id": 1,
      "recipients": [
        {}
      ],
      "templateDocumentData": {},
      "templateMeta": {},
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
| `envelopeId` | string |  |
| `externalId` | string |  |
| `fields` | array<object> |  |
| `id` | number |  |
| `recipients` | array<object> |  |
| `templateDocumentData` | object |  |
| `templateMeta` | object |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `visibility` | string |  |

## Native endpoint

Through the native Documenso API, this operation is `GET /template/:templateId` (base URL `https://app.documenso.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

