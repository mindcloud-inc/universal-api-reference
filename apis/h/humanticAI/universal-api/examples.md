# Humantic AI Universal API Examples

These examples use the MindCloud API key and Humantic AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Analysis



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/fetch-analysis?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/fetch-analysis?${params}`, {
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
      "message": "string",
      "metadata": {
        "analysis_status": "string",
        "analysis_type": "string",
        "confidence": {
          "level": "string",
          "score": 1
        },
        "s3_analysis_status": "string",
        "status": "string",
        "status_code": 1
      },
      "results": {
        "persona": {
          "hiring": {
            "profile_url": "https://example.com"
          },
          "sales": {
            "profile_url": "https://example.com"
          }
        },
        "user_id": "string"
      },
      "status": "string",
      "usage_stats": {
        "user_profile": {
          "consumed": 1,
          "limit": 1,
          "remaining": 1,
          "subscription_status": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Fetch Analysis action reference](actions/fetch-analysis.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/humanticAI/latest/actions/fetch-analysis).

## Create Document Analysis



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/create-document-analysis" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "document": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/create-document-analysis', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "document": "string"
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
      "message": "string",
      "metadata": {
        "first_created_at": "2026-05-07T12:00:00.000Z",
        "last_modified_at": "2026-05-07T12:00:00.000Z"
      },
      "results": {
        "userid": "string",
        "username": "Ava Chen"
      },
      "status": "string",
      "usage_stats": {
        "user_profile": {
          "consumed": 1,
          "limit": 1,
          "remaining": 1,
          "subscription_status": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Document Analysis action reference](actions/create-document-analysis.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/humanticAI/latest/actions/create-document-analysis).
