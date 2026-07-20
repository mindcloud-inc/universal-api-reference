# Conveyor Universal API Examples

These examples use the MindCloud API key and Conveyor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Connections

Retrieves connections from Conveyor with optional filters.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-connections?${params}`, {
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
      "connections": [
        {
          "_type": "string",
          "authorizations_count": 1,
          "authorizations_removed_count": 1,
          "authorizations_with_access_count": 1,
          "created_at": "2026-05-07T12:00:00.000Z",
          "crm_id": "string",
          "crm_link": "https://example.com",
          "domain": "string",
          "id": "string",
          "latest_activity_at": "2026-05-07T12:00:00.000Z",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      ],
      "page": 1,
      "per_page": 1,
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

See the full [List Connections action reference](actions/list-connections.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/conveyor/latest/actions/list-connections).

## Answer Single Question

Answers a one-off question in Conveyor.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/answer-single-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "question": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/answer-single-question', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "question": "string"
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
      "answer": "string",
      "answer_confidence": "string",
      "id": "string",
      "question": "string",
      "structured_answer": {},
      "structured_answers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Answer Single Question action reference](actions/answer-single-question.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/conveyor/latest/actions/answer-single-question).
