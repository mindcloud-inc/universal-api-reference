# Docage: List Documents

Retrieves accessible documents from Docage.

```
GET https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Docage API, this operation is `GET /Documents` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

