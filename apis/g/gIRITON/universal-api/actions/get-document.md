# GIRITON: Get Document

Retrieves a specific document from GIRITON.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-document?${params}`, {
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
| `documentId` | string | yes | Document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agendaId": "string",
      "createdOn": "string",
      "description": "string",
      "entryTimestamp": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "mediaType": "string",
      "name": "Ava Chen",
      "owner": {},
      "recordId": "string",
      "signature": {},
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agendaId` | string | Agenda ID. |
| `createdOn` | string | Document creation date. |
| `description` | string | Document description. |
| `entryTimestamp` | date | Document entry timestamp. |
| `id` | string | Document ID. |
| `mediaType` | string | Document media type. |
| `name` | string | Document name. |
| `owner` | object | Document owner. |
| `recordId` | string | Agenda record ID. |
| `signature` | object | Document signature details. |
| `size` | number | Document size in bytes. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /documents/:documentId` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

