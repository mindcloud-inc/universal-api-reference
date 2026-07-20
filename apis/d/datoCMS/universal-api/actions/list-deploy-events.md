# DatoCMS: List Deploy Events



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-deploy-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-deploy-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-deploy-events?${params}`, {
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
| `eventIds` | string | no | Comma-separated deploy event IDs to return. Accepts multiple values as an array. Example: `123,456`. |
| `eventType` | string | no | Filter deploy events by event type. Example: `response_success`. |
| `buildTriggerId` | string | no | Filter deploy events by build trigger ID. |
| `orderBy` | string | no | Sort expression such as created_at_desc or event_type_asc. Example: `created_at_desc`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdAfter` | date | no | Include events created after this timestamp (ISO-8601). Example: `2026-01-01T00:00:00Z`. |
| `createdBefore` | date | no | Include events created before this timestamp (ISO-8601). Example: `2026-01-31T23:59:59Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Deploy event properties |
| `id` | string | Deploy event ID |
| `type` | string | Resource type |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /build-events` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deploy-events.md) for the provider-specific parameters and requirements.

