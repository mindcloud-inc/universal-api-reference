# Zoho Sign Universal API Examples

These examples use the MindCloud API key and Zoho Sign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Documents

Retrieves documents from Zoho Sign.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-documents?${params}`, {
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
      "code": 1,
      "message": "string",
      "pageContext": {
        "hasMoreRows": true,
        "rowCount": 1,
        "sortColumn": "string",
        "sortOrder": "string",
        "startIndex": 1,
        "totalCount": 1
      },
      "requests": [
        {
          "actions": [
            {}
          ],
          "createdTime": 1,
          "documentIds": [
            {}
          ],
          "emailReminders": true,
          "expirationDays": 1,
          "isSequential": true,
          "modifiedTime": 1,
          "ownerEmail": "ava@example.com",
          "requestId": "string",
          "requestName": "Ava Chen",
          "requestStatus": "string",
          "requestTypeId": "string",
          "requestTypeName": "Ava Chen",
          "selfSign": true,
          "signPercentage": 1
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Documents action reference](actions/list-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoSign/latest/actions/list-documents).

## Correct Document

Marks a document for correction in Zoho Sign.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/correct-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/correct-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestId": "string"
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
      "code": 1,
      "message": "string",
      "requestStatus": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Correct Document action reference](actions/correct-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoSign/latest/actions/correct-document).
