# gotoHuman Universal API Examples

These examples use the MindCloud API key and gotoHuman connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Review Forms

Retrieves review templates from gotoHuman.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/list-review-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/list-review-forms?${params}`, {
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
      "forms": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Review Forms action reference](actions/list-review-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gotoHuman/latest/actions/list-review-forms).

## Create Review Request

Creates a new review request in gotoHuman.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/create-review-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "fields": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/create-review-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "fields": "string"
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
      "extReviewerLinks": [
        {}
      ],
      "gthLink": "https://example.com",
      "reviewId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Review Request action reference](actions/create-review-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gotoHuman/latest/actions/create-review-request).
