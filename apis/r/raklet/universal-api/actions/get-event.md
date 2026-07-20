# Raklet: Get Event



```
GET https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-event?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-event?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "country": "string",
      "currency": "string",
      "description": "string",
      "endDateTime": "2026-05-07T12:00:00.000Z",
      "eventImageUrl": "https://example.com",
      "eventTicketOptionCount": 1,
      "id": "string",
      "isPublic": true,
      "name": "Ava Chen",
      "organisationId": "string",
      "organisationName": "Ava Chen",
      "shortDescription": "string",
      "startDateTime": "2026-05-07T12:00:00.000Z",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `endDateTime` | date |  |
| `eventImageUrl` | string |  |
| `eventTicketOptionCount` | number |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `name` | string |  |
| `organisationId` | string |  |
| `organisationName` | string |  |
| `shortDescription` | string |  |
| `startDateTime` | date |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Raklet API, this operation is `GET /app/organisations/:organisationId/events/:id` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

