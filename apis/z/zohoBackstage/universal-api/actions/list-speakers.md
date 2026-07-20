# Zoho Backstage: List Speakers



```
GET https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-speakers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-speakers?connectionId=$CONNECTION_ID&portalId=string&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-speakers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalId` | string | yes | The Zoho Backstage portal ID. |
| `eventId` | string | yes | The Zoho Backstage event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedOn": "2026-05-07T12:00:00.000Z",
      "alternateTelephone": "string",
      "company": "string",
      "country": "string",
      "description": "string",
      "designation": "string",
      "email": "ava@example.com",
      "facebook": "string",
      "featured": true,
      "firstName": "Ava",
      "id": "string",
      "instagram": "string",
      "joinedOn": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "linkedin": "https://example.com",
      "medium": "string",
      "skills": "string",
      "status": 1,
      "statusString": "string",
      "telegram": "string",
      "telephone": "string",
      "twitter": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedOn` | date |  |
| `alternateTelephone` | string |  |
| `company` | string |  |
| `country` | string |  |
| `description` | string |  |
| `designation` | string |  |
| `email` | string |  |
| `facebook` | string |  |
| `featured` | boolean |  |
| `firstName` | string |  |
| `id` | string |  |
| `instagram` | string |  |
| `joinedOn` | date |  |
| `lastName` | string |  |
| `linkedin` | string |  |
| `medium` | string |  |
| `skills` | string |  |
| `status` | number |  |
| `statusString` | string |  |
| `telegram` | string |  |
| `telephone` | string |  |
| `twitter` | string |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `GET /v3/portals/:portal_id/events/:event_id/speakers` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-speakers.md) for the provider-specific parameters and requirements.

