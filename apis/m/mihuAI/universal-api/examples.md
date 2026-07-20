# Mihu AI Universal API Examples

These examples use the MindCloud API key and Mihu AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Paginated List of Calls



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-paginated-list-of-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-paginated-list-of-calls?${params}`, {
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
      "agent": {
        "name": "Ava Chen",
        "uuid": "string"
      },
      "analysis": "string",
      "communication": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "duration": 1,
      "handledBy": "string",
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Paginated List of Calls action reference](actions/get-paginated-list-of-calls.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mihuAI/latest/actions/get-paginated-list-of-calls).

## Add Tag to Contact



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/add-tag-to-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/add-tag-to-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
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
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customField_1": "string",
      "customField_2": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "numberType": "string",
      "phoneNumber": "string",
      "preferredContactChannel": "string",
      "preferredContactTime": "string",
      "primaryLanguage": "string",
      "status": "string",
      "surname": "Ava Chen",
      "tags": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "timezone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Tag to Contact action reference](actions/add-tag-to-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mihuAI/latest/actions/add-tag-to-contact).
