# DataScope Forms Universal API Examples

These examples use the MindCloud API key and DataScope Forms connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Answers

Retrieves submitted answers from DataScope Forms.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-answers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-answers?${params}`, {
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
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "form_answer_id": 1,
      "form_id": 1,
      "form_name": "Ava Chen",
      "form_state": "string",
      "latitude": 1,
      "longitude": 1,
      "user_identifier": "string",
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Answers action reference](actions/list-answers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataScopeForms/latest/actions/list-answers).

## Bulk Update List Elements

Updates list elements in DataScope Forms by replacing the full list.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/bulk-update-list-elements" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_objects[]": [
    {}
  ],
  "metadata_type": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/bulk-update-list-elements', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_objects[]": [{}],
    "metadata_type": "string",
    "name": "Ava Chen"
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
      "code": "string",
      "description": "string",
      "id": 1,
      "length": 1,
      "list_type": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Bulk Update List Elements action reference](actions/bulk-update-list-elements.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataScopeForms/latest/actions/bulk-update-list-elements).
