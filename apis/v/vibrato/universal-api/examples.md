# Vibrato Universal API Examples

These examples use the MindCloud API key and Vibrato connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List contacts

Retrieves a list of contacts from Vibrato.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/list-contacts?${params}`, {
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
      "country_code": "string",
      "current_campaign_calls": [
        {}
      ],
      "custom_fields": [
        {}
      ],
      "display_name": "Ava Chen",
      "first_name": "Ava",
      "last_name": "Chen",
      "merge_key": "string",
      "phone_number": "string",
      "tags": [
        "string"
      ],
      "uuid": "string",
      "validation_errors": {}
    }
  ],
  "meta": {}
}
```

See the full [List contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vibrato/latest/actions/list-contacts).

## Create call

Creates a new call in Vibrato.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/create-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "countryCode": "string",
  "phoneNumber": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/create-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "countryCode": "string",
    "phoneNumber": "string",
    "prompt": "string"
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
      "api_idempotency_key": "string",
      "completed_at": "2026-05-07T12:00:00.000Z",
      "country_code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "id": 1,
      "labels": [
        "string"
      ],
      "language_name": "Ava Chen",
      "locale": "string",
      "locale_name": "Ava Chen",
      "phone_number": "string",
      "prompt": "string",
      "recording_url": "https://example.com",
      "started_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "succeeded": true,
      "summary": "string",
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create call action reference](actions/create-call.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vibrato/latest/actions/create-call).
