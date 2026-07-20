# Workiz Universal API Examples

These examples use the MindCloud API key and Workiz connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Team Members

Finds all team members in Workiz.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/list-team-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiz/latest/actions/list-team-members?${params}`, {
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
      "created": "string",
      "email": "ava@example.com",
      "fieldTech": true,
      "id": "string",
      "name": "Ava Chen",
      "role": "string",
      "serviceAreas": [
        "string"
      ],
      "skills": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Team Members action reference](actions/list-team-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workiz/latest/actions/list-team-members).

## Activate Lead

Activates an existing lead in Workiz.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/activate-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workiz/latest/actions/activate-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
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
      "code": "string",
      "flag": true,
      "msg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Activate Lead action reference](actions/activate-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workiz/latest/actions/activate-lead).
