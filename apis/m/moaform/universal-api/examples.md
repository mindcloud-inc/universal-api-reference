# Moaform Universal API Examples

These examples use the MindCloud API key and Moaform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms

Retrieves forms from your Moaform account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-forms?${params}`, {
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
      "items": [
        {
          "collection": {
            "endAt": "2026-05-07T12:00:00.000Z",
            "responsesCount": 1,
            "startAt": "2026-05-07T12:00:00.000Z"
          },
          "createdAt": "2026-05-07T12:00:00.000Z",
          "groups": [
            "string"
          ],
          "id": "string",
          "lastResponsedAt": "2026-05-07T12:00:00.000Z",
          "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
          "links": {
            "answerUrl": "https://example.com",
            "reportUrl": "https://example.com",
            "self": "https://example.com"
          },
          "longId": "string",
          "name": "Ava Chen",
          "owned": true,
          "status": "string"
        }
      ],
      "pageCount": 1,
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moaform/latest/actions/list-forms).

## Create Webhook

Creates a webhook for a form in Moaform.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moaform/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "endpoint": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moaform/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "endpoint": "string"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "endpoint": "string",
      "id": "string",
      "retentionDays": 1,
      "secret": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "verifySsl": true
    }
  ],
  "meta": {}
}
```

See the full [Create Webhook action reference](actions/create-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moaform/latest/actions/create-webhook).
