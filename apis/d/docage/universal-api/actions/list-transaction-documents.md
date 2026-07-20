# Docage: List Transaction Documents

Downloads all documents from a Docage transaction.

```
GET https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-transaction-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-transaction-documents?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-transaction-documents?${params}`, {
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
| `id` | string | yes | The Docage transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CultureInfo": "string",
      "FileName": "Ava Chen",
      "FriendlyName": "Ava Chen",
      "IsSignedVersion": true,
      "KeepFileNameDuringReplacement": true,
      "Name": "Ava Chen",
      "NbPages": 1,
      "Order": 1,
      "TemplateFileId": "string",
      "TransactionDocumentId": "string",
      "TransactionId": "string",
      "Type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CultureInfo` | string |  |
| `FileName` | string |  |
| `FriendlyName` | string |  |
| `IsSignedVersion` | boolean |  |
| `KeepFileNameDuringReplacement` | boolean |  |
| `Name` | string |  |
| `NbPages` | number |  |
| `Order` | number |  |
| `TemplateFileId` | string |  |
| `TransactionDocumentId` | string |  |
| `TransactionId` | string |  |
| `Type` | number |  |

## Native endpoint

Through the native Docage API, this operation is `GET /Transactions/GetTransactionFiles/:id` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transaction-documents.md) for the provider-specific parameters and requirements.

