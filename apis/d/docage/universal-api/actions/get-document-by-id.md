# Docage: Get Document By ID

Retrieves a document from Docage by ID.

```
GET https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-document-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-document-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/get-document-by-id?${params}`, {
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
| `id` | string | yes | The Docage document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BoxDocuments": [
        "string"
      ],
      "Boxes": [
        "string"
      ],
      "Content": "string",
      "CultureInfo": "string",
      "EntityState": 1,
      "GeneratedByFormId": "string",
      "IsTemplate": true,
      "Name": "Ava Chen",
      "Notes": "string",
      "ParentOrganizationId": "string",
      "TemplateId": "string",
      "TransactionFiles": [
        "string"
      ],
      "Type": 1,
      "UsedInForms": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BoxDocuments` | array |  |
| `Boxes` | array |  |
| `Content` | string |  |
| `CultureInfo` | string |  |
| `EntityState` | number |  |
| `GeneratedByFormId` | string |  |
| `IsTemplate` | boolean |  |
| `Name` | string |  |
| `Notes` | string |  |
| `ParentOrganizationId` | string |  |
| `TemplateId` | string |  |
| `TransactionFiles` | array |  |
| `Type` | number |  |
| `UsedInForms` | array |  |

## Native endpoint

Through the native Docage API, this operation is `GET /Documents/ById/:id` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-by-id.md) for the provider-specific parameters and requirements.

