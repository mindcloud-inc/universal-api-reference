# AidaForm Universal API Examples

These examples use the MindCloud API key and AidaForm connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms

Retrieves forms from your AidaForm account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aidaForm/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aidaForm/latest/actions/list-forms?${params}`, {
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
      "count": 1,
      "items": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "dashboardToken": {},
          "data": {
            "backgroundWidth": 1,
            "code": "string",
            "language": "string",
            "name": "Ava Chen",
            "notificationsEnabled": true,
            "submit": {
              "label": "string",
              "prevLabel": "string"
            },
            "theme": "string"
          },
          "domain": "string",
          "fields": [
            {
              "id": "string",
              "label": "string",
              "properties": {
                "align": "string",
                "firstName": "Ava",
                "lastName": "Chen",
                "placeholderFirstName": "Ava",
                "placeholderLastName": "Chen",
                "required": true
              },
              "type": "string"
            }
          ],
          "id": "string",
          "inventory": {},
          "owner": "string",
          "responses": 1,
          "shareToken": {},
          "shareTokenCreated": {},
          "status": "string",
          "unread": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "uri": "string",
          "version": 1,
          "views": 1
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aidaForm/latest/actions/list-forms).
