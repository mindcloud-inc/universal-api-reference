# Timekit Universal API Examples

These examples use the MindCloud API key and Timekit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current App

Retrieves the current app from Timekit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-current-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-current-app?${params}`, {
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
      "api_trial_expires_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "creator_resource_id": "string",
      "id": "string",
      "role": "string",
      "settings": {},
      "slug": "string",
      "test_mode": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "webhook_secret": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current App action reference](actions/get-current-app.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timekit/latest/actions/get-current-app).

## Add Project Resource

Adds a resource to a project in Timekit.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/add-project-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "resourceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timekit/latest/actions/add-project-resource', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "resourceId": "string"
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
      "allow_conference": 1,
      "allow_double_bookings": true,
      "availability": {
        "buffer": "string",
        "closest_time_interval": "string",
        "from": "string",
        "ignore_all_day_events": true,
        "length": "string",
        "mode": "string",
        "to": "string"
      },
      "booking": {
        "description": "string",
        "graph": "string",
        "rescheduling_url": "https://example.com",
        "what": "string",
        "where": "string"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "customer_fields": {
        "email": {
          "format": "ava@example.com",
          "prefilled": "ava@example.com",
          "readonly": true,
          "required": true,
          "title": "ava@example.com"
        },
        "name": {
          "format": "Ava Chen",
          "prefilled": "Ava Chen",
          "readonly": true,
          "required": true,
          "title": "Ava Chen"
        }
      },
      "distance": 1,
      "enabled_email_notification": true,
      "id": "string",
      "latitude": "string",
      "longitude": "string",
      "meta": {
        "wizardRun": "string"
      },
      "name": "Ava Chen",
      "reservation_time": "string",
      "slug": "string",
      "ui": {
        "availability_view": "string",
        "localization": {
          "allocated_resource_prefix": "string",
          "submit_button": "string",
          "success_message": "string"
        },
        "show_credits": true,
        "time_date_format": "string"
      },
      "updated_at": "2026-05-07T12:00:00.000Z",
      "use_hours_from": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Project Resource action reference](actions/add-project-resource.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timekit/latest/actions/add-project-resource).
