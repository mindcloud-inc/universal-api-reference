# Poodll Universal API Examples

These examples use the MindCloud API key and Poodll connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Site Info

Retrieves site information and services from Poodll.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-site-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-site-info?${params}`, {
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
      "fullname": "Ava Chen",
      "functions": [
        {}
      ],
      "sitename": "Ava Chen",
      "siteurl": "https://example.com",
      "userid": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Site Info action reference](actions/get-site-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/poodll/latest/actions/get-site-info).

## Add Cohort Members

Adds members to a cohort in Poodll.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/poodll/latest/actions/add-cohort-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "members[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/poodll/latest/actions/add-cohort-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "members[]": [{}]
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
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Cohort Members action reference](actions/add-cohort-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/poodll/latest/actions/add-cohort-members).
