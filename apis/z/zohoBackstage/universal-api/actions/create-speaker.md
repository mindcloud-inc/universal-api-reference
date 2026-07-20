# Zoho Backstage: Create Speaker



```
POST https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-speaker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-speaker" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": "string",
  "eventId": "string",
  "email": "ava@example.com",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-speaker', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": "string",
    "eventId": "string",
    "email": "ava@example.com",
    "name": "Ava Chen"
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
| `email` | string | yes |  |
| `name` | string | yes |  |
| `lastName` | string | no |  |
| `country` | string | no |  |
| `featured` | boolean | no |  |
| `company` | string | no |  |
| `designation` | string | no |  |
| `description` | string | no |  |
| `telephone` | string | no |  |
| `alternateTelephone` | string | no |  |
| `skills` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added_on": "2026-05-07T12:00:00.000Z",
      "alternate_telephone": "string",
      "company": "string",
      "country": "string",
      "description": "string",
      "designation": "string",
      "email": "ava@example.com",
      "featured": true,
      "first_name": "Ava",
      "id": "string",
      "joined_on": "2026-05-07T12:00:00.000Z",
      "last_name": "Chen",
      "skills": "string",
      "status": 1,
      "status_string": "string",
      "telephone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added_on` | date |  |
| `alternate_telephone` | string |  |
| `company` | string |  |
| `country` | string |  |
| `description` | string |  |
| `designation` | string |  |
| `email` | string |  |
| `featured` | boolean |  |
| `first_name` | string |  |
| `id` | string |  |
| `joined_on` | date |  |
| `last_name` | string |  |
| `skills` | string |  |
| `status` | number |  |
| `status_string` | string |  |
| `telephone` | string |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `POST /v3/portals/:portal_id/events/:event_id/speakers` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-speaker.md) for the provider-specific parameters and requirements.

