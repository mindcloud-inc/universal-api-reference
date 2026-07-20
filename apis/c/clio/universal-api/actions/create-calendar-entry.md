# Clio Manage: Create Calendar Entry

Creates a new calendar entry in Clio Manage.

```
POST https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-calendar-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-calendar-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.summary": "string",
  "data.start_at": "string",
  "data.end_at": "string",
  "data.calendar_owner.id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-calendar-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.summary": "string",
    "data.start_at": "string",
    "data.end_at": "string",
    "data.calendar_owner.id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.summary` | string | yes | Short summary of the calendar entry. |
| `data.start_at` | string | yes | Calendar entry start timestamp in ISO-8601 format. |
| `data.end_at` | string | yes | Calendar entry end timestamp in ISO-8601 format. |
| `data.calendar_owner.id` | number | yes | Calendar that owns the calendar entry. |
| `data.description` | string | no | Detailed description of the calendar entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Clio Manage API, this operation is `POST /calendar_entries.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-calendar-entry.md) for the provider-specific parameters and requirements.

