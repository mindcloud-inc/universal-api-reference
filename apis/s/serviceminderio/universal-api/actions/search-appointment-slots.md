# serviceminder.io: Search Appointment Slots

Finds appointment slots in ServiceMinder by date range and service.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/search-appointment-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/search-appointment-slots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/search-appointment-slots?${params}`, {
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
| `startDate` | date | no | Slot-search start date. |
| `finishDate` | date | no | Slot-search finish date. |
| `serviceId` | number | no | Service identifier for slot search. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native serviceminder.io API returns.

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /appointments/slotsearch` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-appointment-slots.md) for the provider-specific parameters and requirements.

