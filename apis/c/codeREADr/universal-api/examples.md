# CodeREADr Universal API Examples

These examples use the MindCloud API key and CodeREADr connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Limits

Retrieves API usage limits from CodeREADr.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/retrieve-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/retrieve-limits?${params}`, {
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
      "_declaration": {
        "_attributes": {
          "encoding": "string",
          "version": "string"
        }
      },
      "xml": {
        "day": {
          "_attributes": {
            "left": "string",
            "limit": "string"
          }
        },
        "minute": {
          "_attributes": {
            "left": "string",
            "limit": "string"
          }
        },
        "status": {
          "_text": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Limits action reference](actions/retrieve-limits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/codeREADr/latest/actions/retrieve-limits).

## Add Question to Service

Adds a question to a scanning service in CodeREADr.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/add-question-to-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "serviceId": "2231648",
  "questionId": "123456"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/add-question-to-service', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "serviceId": "2231648",
    "questionId": "123456"
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
      "_declaration": {
        "_attributes": {
          "encoding": "string",
          "version": "string"
        }
      },
      "xml": {
        "status": {
          "_text": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Question to Service action reference](actions/add-question-to-service.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/codeREADr/latest/actions/add-question-to-service).
