# Pipeline CRM Universal API Examples

These examples use the MindCloud API key and Pipeline CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Activities

Finds activity notes in Pipeline CRM for a deal, person, or company.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/list-activities?${params}`, {
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
      "account_id": 1,
      "comments": {},
      "company_id": 1,
      "content": "string",
      "created_at": "string",
      "deal_id": 1,
      "id": 1,
      "is_sent_message": true,
      "milestone_id": 1,
      "note_category_id": 1,
      "note_category": {
        "id": 1,
        "name": "Ava Chen"
      },
      "notify_user_ids": [
        [
          "string"
        ]
      ],
      "person_id": 1,
      "possible_notify_user_ids": [
        [
          "string"
        ]
      ],
      "primary_association_id": 1,
      "primary_association_type": "string",
      "title": "string",
      "updated_at": "string",
      "user_id": 1,
      "user": {
        "avatar_thumb_url": "https://example.com",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Activities action reference](actions/list-activities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipelineCRM/latest/actions/list-activities).

## Create Activity

Creates a new activity note in Pipeline CRM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "account_id": 1,
      "comments": {},
      "company_id": 1,
      "content": "string",
      "created_at": "string",
      "deal_id": 1,
      "id": 1,
      "is_sent_message": true,
      "milestone_id": 1,
      "note_category_id": 1,
      "note_category": {
        "id": 1,
        "name": "Ava Chen"
      },
      "notify_user_ids": [
        [
          "string"
        ]
      ],
      "person_id": 1,
      "possible_notify_user_ids": [
        [
          "string"
        ]
      ],
      "primary_association_id": 1,
      "primary_association_type": "string",
      "title": "string",
      "updated_at": "string",
      "user_id": 1,
      "user": {
        "avatar_thumb_url": "https://example.com",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Activity action reference](actions/create-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipelineCRM/latest/actions/create-activity).
