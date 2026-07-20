# Oboloo Universal API Examples

These examples use the MindCloud API key and Oboloo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Categories

Retrieves categories from Oboloo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-categories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "code": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "creator": {},
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "status": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Categories action reference](actions/list-categories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oboloo/latest/actions/list-categories).

## Create Contract Document Type

Creates a new contract document type in Oboloo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-contract-document-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contract_document_type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-contract-document-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contract_document_type": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "documentType": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "createdBy": 1,
        "createdType": "string",
        "id": 1,
        "name": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contract Document Type action reference](actions/create-contract-document-type.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oboloo/latest/actions/create-contract-document-type).
