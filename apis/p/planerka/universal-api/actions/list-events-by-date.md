# Planerka: List events by date

Retrieves events from Planerka for a specific date.

```
GET https://connect.mindcloud.co/v1/universal/planerka/latest/actions/list-events-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planerka `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planerka/latest/actions/list-events-by-date?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planerka/latest/actions/list-events-by-date?${params}`, {
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
| `date` | string | no | Date in d.m.Y format used to list events for a single day. Example: `21.04.2026`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Planerka API returns.

## Native endpoint

Through the native Planerka API, this operation is `GET /event/` (base URL `https://planerka.app/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events-by-date.md) for the provider-specific parameters and requirements.

