# OfficeMaps Universal API Examples

These examples use the MindCloud API key and OfficeMaps connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Departments

Retrieves departments from OfficeMaps with membership data.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-departments?${params}`, {
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
      "administrators": [
        "string"
      ],
      "departmentId": "string",
      "isHidden": true,
      "managers": [
        "string"
      ],
      "members": [
        "string"
      ],
      "name": "Ava Chen",
      "parentDepartmentId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Departments action reference](actions/get-departments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/officeMaps/latest/actions/get-departments).

## Add Department Administrator

Adds an administrator to a department in OfficeMaps.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/add-department-administrator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "departmentId": "string",
  "personId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/add-department-administrator', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "departmentId": "string",
    "personId": "string"
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
      "failure": true,
      "notFound": true,
      "success": true,
      "unauthorized": true,
      "value": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Department Administrator action reference](actions/add-department-administrator.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/officeMaps/latest/actions/add-department-administrator).
