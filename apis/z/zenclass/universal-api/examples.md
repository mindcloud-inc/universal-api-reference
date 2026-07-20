# Zenclass Universal API Examples

These examples use the MindCloud API key and Zenclass connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get school

Retrieves your school details from Zenclass.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/get-school?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/get-school?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get school action reference](actions/get-school.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zenclass/latest/actions/get-school).

## Change course tariff

Updates a student's course tariff in Zenclass.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/change-course-tariff" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "string",
  "email": "ava@example.com",
  "tariffId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/change-course-tariff', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "string",
    "email": "ava@example.com",
    "tariffId": "string"
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
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Change course tariff action reference](actions/change-course-tariff.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zenclass/latest/actions/change-course-tariff).
