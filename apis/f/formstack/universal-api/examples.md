# Formstack Universal API Examples

These examples use the MindCloud API key and Formstack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms

Retrieves forms from Formstack with filtering and sorting.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstack/latest/actions/list-forms?${params}`, {
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
      "active": true,
      "created": "2026-05-07T12:00:00.000Z",
      "dataUrl": "https://example.com",
      "db": true,
      "deleted": true,
      "editUrl": "https://example.com",
      "encrypted": true,
      "folder": 1,
      "id": 1,
      "inactive": true,
      "isWorkflowForm": true,
      "isWorkflowPublished": true,
      "language": "string",
      "name": "Ava Chen",
      "numberOfColumns": "string",
      "progressMeter": "string",
      "shouldDisplayOneQuestionAtATime": true,
      "submissions": "string",
      "submissionsCount": 1,
      "submissionsUnread": "string",
      "submitButtonTitle": "string",
      "summaryUrl": "https://example.com",
      "thumbnailUrl": "https://example.com",
      "timezone": "string",
      "unreadSubmissionsCount": 1,
      "updated": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "version": "string",
      "viewKey": "string",
      "views": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formstack/latest/actions/list-forms).

## Copy Form

Creates a copy of a form in Formstack.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/copy-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstack/latest/actions/copy-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": 1
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
      "canEdit": true,
      "created": "2026-05-07T12:00:00.000Z",
      "fields": [
        {}
      ],
      "folder": 1,
      "formExtras": {},
      "formSettings": {},
      "hasApprovers": true,
      "id": 1,
      "isEncrypted": true,
      "isWorkflowForm": true,
      "isWorkflowPublished": true,
      "name": "Ava Chen",
      "permissions": 1,
      "submissionsCount": 1,
      "submitButtonTitle": "string",
      "todaySubmissionsCount": 1,
      "unreadSubmissionsCount": 1,
      "updated": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "version": 1,
      "viewKey": "string"
    }
  ],
  "meta": {}
}
```

See the full [Copy Form action reference](actions/copy-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formstack/latest/actions/copy-form).
