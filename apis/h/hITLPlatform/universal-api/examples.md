# HITL Platform Universal API Examples

These examples use the MindCloud API key and HITL Platform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test API Key



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/test-api-key?${params}`, {
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
      "account_status": "string",
      "api_key_id": "string",
      "email": "ava@example.com",
      "permissions": [
        [
          "string"
        ]
      ],
      "rate_limit": {
        "limit": 1,
        "remaining": 1,
        "reset_at": "2026-05-07T12:00:00.000Z"
      },
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test API Key action reference](actions/test-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hITLPlatform/latest/actions/test-api-key).

## Add Request Feedback



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/add-request-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/add-request-feedback', {
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
      "feedback": {
        "accuracy": 1,
        "category": "string",
        "comment": "string",
        "helpfulness": 1,
        "rating": 1,
        "tags": [
          [
            "string"
          ]
        ],
        "timeliness": 1,
        "would_recommend": true
      },
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Request Feedback action reference](actions/add-request-feedback.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hITLPlatform/latest/actions/add-request-feedback).
