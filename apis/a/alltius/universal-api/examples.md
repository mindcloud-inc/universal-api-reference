# Alltius Universal API Examples

These examples use the MindCloud API key and Alltius connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Connection

Submits a test prompt to verify an Alltius connection.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alltius/latest/actions/verify-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alltius/latest/actions/verify-connection?${params}`, {
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
      "answer_confidence_score": 1,
      "answer_type": "string",
      "blocks_response": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_at_response": "2026-05-07T12:00:00.000Z",
      "cta_list": {},
      "id": "string",
      "image_metadata_list": [
        {}
      ],
      "intent_confidence": 1,
      "intent_confidence_label": "string",
      "intent_type": "string",
      "llm_response_model_family": "string",
      "metadata": {},
      "multi_cta_list": [
        {}
      ],
      "post": "string",
      "rating": 1,
      "recommendations": [
        {}
      ],
      "relevant_links_response": "https://example.com",
      "response": "string",
      "thread_id": "string",
      "v2_chat_session_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Connection action reference](actions/verify-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/alltius/latest/actions/verify-connection).

## Rate Response

Updates feedback for an Alltius assistant response.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/alltius/latest/actions/rate-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "postId": "69d8f8f9d221c6bbc7c37d70",
  "rating": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alltius/latest/actions/rate-response', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "postId": "69d8f8f9d221c6bbc7c37d70",
    "rating": "1"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Rate Response action reference](actions/rate-response.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/alltius/latest/actions/rate-response).
