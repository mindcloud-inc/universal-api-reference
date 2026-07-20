# Hipsy: List Orders

Retrieves orders from a Hipsy organisation.

```
GET https://connect.mindcloud.co/v1/universal/hipsy/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hipsy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hipsy/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&organisationSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organisationSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hipsy/latest/actions/list-orders?${params}`, {
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
| `organisationSlug` | string | yes | Slug of the organisation whose orders should be listed. |
| `event` | number | no | Return only orders for a specific event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "event_id": 1,
      "event_name": "Ava Chen",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "locale": "string",
      "newsletter": 1,
      "revenue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Date and time of the order. |
| `event_id` | number | The ID of the event. |
| `event_name` | string | The name of the event. |
| `first_name` | string | First name of the buyer. |
| `id` | number | The ID of the order. |
| `last_name` | string | Last name of the buyer. |
| `locale` | string | Language used when buying the ticket. |
| `newsletter` | number | Whether the buyer subscribed to the newsletter, returned as 1 or 0. |
| `revenue` | string | Revenue paid out to the organisation, excluding service costs. |

## Native endpoint

Through the native Hipsy API, this operation is `GET /organisation/:organisationSlug/orders` (base URL `https://api.hipsy.nl/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

