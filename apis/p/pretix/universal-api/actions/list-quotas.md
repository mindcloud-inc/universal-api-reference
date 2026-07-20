# pretix: List Quotas

Retrieves quotas from a pretix event.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-quotas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-quotas?connectionId=$CONNECTION_ID&limit=25&offset=0&organizer=string&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizer": "string",
  "event": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-quotas?${params}`, {
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
| `organizer` | string | yes | pretix organizer slug. |
| `event` | string | yes | pretix event slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": true,
      "availableNumber": 1,
      "closed": true,
      "closeWhenSoldOut": true,
      "id": 1,
      "ignoreForEventAvailability": true,
      "items": [
        1
      ],
      "name": "Ava Chen",
      "releaseAfterExit": true,
      "size": 1,
      "subevent": 1,
      "variations": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean |  |
| `availableNumber` | number |  |
| `closed` | boolean |  |
| `closeWhenSoldOut` | boolean |  |
| `id` | number |  |
| `ignoreForEventAvailability` | boolean |  |
| `items[]` | number |  |
| `name` | string |  |
| `releaseAfterExit` | boolean |  |
| `size` | number |  |
| `subevent` | number |  |
| `variations[]` | number |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/quotas/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-quotas.md) for the provider-specific parameters and requirements.

