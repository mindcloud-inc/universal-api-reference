# pretix: Get Quota Availability

Retrieves quota availability from pretix.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-quota-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-quota-availability?connectionId=$CONNECTION_ID&organizer=string&event=string&quota=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizer": "string",
  "event": "string",
  "quota": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-quota-availability?${params}`, {
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
| `quota` | string | yes | pretix quota ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": true,
      "availableNumber": 1
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

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/quotas/:quota/availability/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quota-availability.md) for the provider-specific parameters and requirements.

