# Ticketmaster: Get Segment

Retrieves details for a specific segment from Ticketmaster.

```
GET https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/get-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticketmaster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/get-segment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/get-segment?${params}`, {
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
| `id` | string | yes | The unique identifier for the segment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "genres": [
        {}
      ],
      "id": "string",
      "locale": "string",
      "name": "Ava Chen",
      "primaryId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `genres` | array<object> |  |
| `id` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `primaryId` | string |  |

## Native endpoint

Through the native Ticketmaster API, this operation is `GET /discovery/v2/classifications/segments/:id` (base URL `https://app.ticketmaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-segment.md) for the provider-specific parameters and requirements.

