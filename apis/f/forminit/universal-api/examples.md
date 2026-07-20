# Forminit Universal API Examples

These examples use the MindCloud API key and Forminit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Submissions

Retrieves submissions for a specific Forminit form.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forminit/latest/actions/list-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forminit/latest/actions/list-submissions?${params}`, {
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
      "apiVersion": "string",
      "fields": [
        {
          "label": "string",
          "name": "Ava Chen",
          "sortOrder": 1,
          "type": "string"
        }
      ],
      "formId": "string",
      "pagination": {
        "count": 1,
        "currentPage": 1,
        "firstPage": 1,
        "lastPage": 1,
        "size": 1,
        "total": 1
      },
      "submissions": [
        {
          "blocks": {},
          "id": "string",
          "isSeen": true,
          "isStarred": true,
          "submissionDate": "2026-05-07T12:00:00.000Z",
          "submissionStatus": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Submissions action reference](actions/list-submissions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/forminit/latest/actions/list-submissions).

## Submit Form

Creates a new submission for a Forminit form.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/forminit/latest/actions/submit-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "kua953xaju5",
  "blocks": "[object Object],[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/forminit/latest/actions/submit-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "kua953xaju5",
    "blocks": "[object Object],[object Object]"
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
      "redirectUrl": "https://example.com",
      "submission": {
        "blocks": {},
        "date": "string",
        "hashId": "string",
        "submissionInfo": {
          "ip": "string",
          "location": {
            "city": {
              "name": "Ava Chen"
            },
            "country": {
              "iso": "string",
              "name": "Ava Chen"
            },
            "geo": {
              "lat": 1,
              "lng": 1
            },
            "timezone": "string"
          },
          "referer": "string",
          "sdk_version": "string",
          "user_agent": "string"
        }
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Submit Form action reference](actions/submit-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/forminit/latest/actions/submit-form).
