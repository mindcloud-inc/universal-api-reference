# Documenso: Create Document From Template

Creates a document from a template in Documenso.

```
POST https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-document-from-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenso `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-document-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": 1,
  "recipients[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-document-from-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": 1,
    "recipients[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | number | yes |  |
| `recipients[]` | array<object> | yes |  |
| `distributeDocument` | boolean | no |  |
| `externalId` | string | no |  |
| `folderId` | string | no |  |
| `prefillFields[]` | array<object> | no |  |
| `override` | object | no |  |
| `formValues` | object | no |  |

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
      "source": "string",
      "status": "string",
      "templateId": 1,
      "title": "string",
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
| `source` | string |  |
| `status` | string |  |
| `templateId` | number |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `visibility` | string |  |

## Native endpoint

Through the native Documenso API, this operation is `POST /template/use` (base URL `https://app.documenso.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-from-template.md) for the provider-specific parameters and requirements.

