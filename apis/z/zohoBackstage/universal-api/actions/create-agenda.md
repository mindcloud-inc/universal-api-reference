# Zoho Backstage: Create Agenda



```
POST https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-agenda
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-agenda" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": "string",
  "eventId": "string",
  "index": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-agenda', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": "string",
    "eventId": "string",
    "index": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalId` | string | yes | The Zoho Backstage portal ID. |
| `eventId` | string | yes | The Zoho Backstage event ID. |
| `index` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agenda_id": "string",
      "created_time": "2026-05-07T12:00:00.000Z",
      "index": 1,
      "last_modified_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agenda_id` | string |  |
| `created_time` | date |  |
| `index` | number |  |
| `last_modified_time` | date |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `POST /v3/portals/:portal_id/events/:event_id/agendas` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agenda.md) for the provider-specific parameters and requirements.

