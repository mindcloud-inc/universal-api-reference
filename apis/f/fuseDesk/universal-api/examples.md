# FuseDesk Universal API Examples

These examples use the MindCloud API key and FuseDesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Active Departments

Retrieves active departments from your FuseDesk account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-active-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-active-departments?${params}`, {
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
      "allReps": true,
      "dateArchived": "2026-05-07T12:00:00.000Z",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "feedbackDelay": 1,
      "feedbackFrequency": 1,
      "feedbackSample": 1,
      "feedbackTemplateId": 1,
      "footerHtml": "string",
      "id": 1,
      "name": "Ava Chen",
      "newCaseNoteTemplateId": 1,
      "noteTemplateId": 1,
      "phone": "string",
      "replyTemplateId": 1,
      "repUserIds": [
        1
      ],
      "stale": 1,
      "staleWarning": 1,
      "templateCategory": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Active Departments action reference](actions/list-active-departments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fuseDesk/latest/actions/list-active-departments).

## Add Case Note

Creates a note on an existing FuseDesk case.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/add-case-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "caseId": 1,
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/add-case-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "caseId": 1,
    "note": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Case Note action reference](actions/add-case-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fuseDesk/latest/actions/add-case-note).
