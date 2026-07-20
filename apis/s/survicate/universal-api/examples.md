# Survicate Universal API Examples

These examples use the MindCloud API key and Survicate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Surveys

Retrieves surveys from your Survicate workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-surveys?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "id": "string",
      "launch": {
        "endAt": "2026-05-07T12:00:00.000Z",
        "responsesLimit": 1,
        "startAt": "2026-05-07T12:00:00.000Z"
      },
      "name": "Ava Chen",
      "responses": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Surveys action reference](actions/list-surveys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/survicate/latest/actions/list-surveys).
