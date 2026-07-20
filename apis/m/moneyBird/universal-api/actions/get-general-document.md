# MoneyBird: Get General Document

Retrieves a general document from MoneyBird.

```
GET https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/get-general-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoneyBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/get-general-document?connectionId=$CONNECTION_ID&administrationId=string&generalDocumentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "administrationId": "string",
  "generalDocumentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/get-general-document?${params}`, {
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
| `administrationId` | string | yes | Moneybird administration ID. |
| `generalDocumentId` | string | yes | Moneybird general document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrationId": "string",
      "attachments": [
        {}
      ],
      "contact": {},
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "details": [
        {}
      ],
      "documentStyleId": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "events": [
        {}
      ],
      "id": "string",
      "reference": "string",
      "state": "string",
      "totalPriceExclTax": "string",
      "totalPriceInclTax": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1,
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrationId` | string |  |
| `attachments` | array<object> |  |
| `contact` | object |  |
| `contactId` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `date` | date |  |
| `details` | array<object> |  |
| `documentStyleId` | string |  |
| `dueDate` | date |  |
| `events` | array<object> |  |
| `id` | string |  |
| `reference` | string |  |
| `state` | string |  |
| `totalPriceExclTax` | string |  |
| `totalPriceInclTax` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |
| `workflowId` | string |  |

## Native endpoint

Through the native MoneyBird API, this operation is `GET /:administrationId/documents/general_documents/:generalDocumentId.json` (base URL `https://moneybird.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-general-document.md) for the provider-specific parameters and requirements.

