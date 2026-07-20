# Umbrella Universal API Examples

These examples use the MindCloud API key and Umbrella connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Roles

Retrieves user role definitions from Umbrella.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-roles?${params}`, {
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
      "label": "string",
      "organizationId": 1,
      "roleId": 1
    }
  ],
  "meta": {}
}
```

See the full [List Roles action reference](actions/list-roles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/umbrella/latest/actions/list-roles).

## Create Alert Rule

Creates a new alert rule in Umbrella.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/create-alert-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "severity": 1,
  "status": 1,
  "rule_type_id": 1,
  "notification_info.0.type": "string",
  "notification_info.0.recipients.0": "string",
  "conditions.match_type": "string",
  "conditions.rows.0.field": "string",
  "conditions.rows.0.value": "string",
  "conditions.rows.1.field": "string",
  "conditions.rows.1.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/create-alert-rule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "severity": 1,
    "status": 1,
    "rule_type_id": 1,
    "notification_info.0.type": "string",
    "notification_info.0.recipients.0": "string",
    "conditions.match_type": "string",
    "conditions.rows.0.field": "string",
    "conditions.rows.0.value": "string",
    "conditions.rows.1.field": "string",
    "conditions.rows.1.value": "string"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Alert Rule action reference](actions/create-alert-rule.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/umbrella/latest/actions/create-alert-rule).
