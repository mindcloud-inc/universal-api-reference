# CompanyCam Universal API Examples

These examples use the MindCloud API key and CompanyCam connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company

Retrieves the current company from CompanyCam.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-company?${params}`, {
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
      "address": {
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string",
        "streetAddress1": "string",
        "streetAddress2": "string"
      },
      "id": 1,
      "logo": [
        {
          "type": "string",
          "uri": "string",
          "url": "https://example.com"
        }
      ],
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company action reference](actions/get-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/companyCam/latest/actions/get-company).

## Add Comment to Project



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/add-comment-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/add-comment-to-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "commentableId": "string",
      "commentableType": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "creatorType": "string",
      "id": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Comment to Project action reference](actions/add-comment-to-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/companyCam/latest/actions/add-comment-to-project).
