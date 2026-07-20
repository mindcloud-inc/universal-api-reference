# SuperSend Universal API Examples

These examples use the MindCloud API key and SuperSend connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves teams from SuperSend.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-teams?${params}`, {
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
      "about": "string",
      "auto_placement_testing": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "id": "string",
      "inbox_auto_tag_settings": {},
      "inbox_super_views": [
        {
          "filters": {
            "labels": [
              [
                "string"
              ]
            ],
            "lastMessageDirection": "string",
            "mood": "string",
            "statuses": [
              [
                "string"
              ]
            ]
          },
          "icon": "string",
          "id": "string",
          "name": "Ava Chen",
          "order": 1,
          "visible": true
        }
      ],
      "is_default": true,
      "logo": "string",
      "meeting_link": "https://example.com",
      "meeting_link_text": "https://example.com",
      "member_count": 1,
      "name": "Ava Chen",
      "notification_email": "ava@example.com",
      "notification_email_preferences": {
        "errorNotificationsEmail": true,
        "linkedinInboxActivityNotificationsEmail": true,
        "newInboxActivityNotificationsEmail": true,
        "outOfContactsNotificationsEmail": true,
        "successNotificationsEmail": true,
        "warmingNotificationsEmail": true
      },
      "organization": {
        "id": "string",
        "name": "Ava Chen"
      },
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/superSend/latest/actions/list-teams).

## Assign Label to Contact Profile

Assigns a profile label to a SuperSend contact.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/assign-label-to-contact-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "labelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/assign-label-to-contact-profile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "labelId": "string"
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
      "contact_profile_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "label_id": "string",
      "object": "string",
      "org_id": "string",
      "team_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Assign Label to Contact Profile action reference](actions/assign-label-to-contact-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/superSend/latest/actions/assign-label-to-contact-profile).
