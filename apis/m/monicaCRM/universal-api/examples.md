# Monica CRM Universal API Examples

These examples use the MindCloud API key and Monica CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Me

Retrieves your user profile from Monica CRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-me?${params}`, {
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
      "data": {
        "account": {
          "id": 1
        },
        "created_at": "string",
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": 1,
        "is_policy_compliant": true,
        "last_name": "Chen",
        "locale": "string",
        "name": "Ava Chen",
        "object": "string",
        "timezone": "string",
        "updated_at": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Me action reference](actions/get-me.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/monicaCRM/latest/actions/get-me).

## Create Activity Type

Creates a new activity type in Monica CRM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/create-activity-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityTypeCategoryId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/create-activity-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityTypeCategoryId": "string",
    "name": "Ava Chen"
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
      "data": {
        "activity_type_category": {
          "id": 1,
          "name": "Ava Chen"
        },
        "created_at": "string",
        "id": 1,
        "location_type": "string",
        "name": "Ava Chen",
        "object": "string",
        "updated_at": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Activity Type action reference](actions/create-activity-type.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/monicaCRM/latest/actions/create-activity-type).
