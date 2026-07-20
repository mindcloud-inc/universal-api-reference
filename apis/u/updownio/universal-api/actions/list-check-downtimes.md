# updown.io: List Check Downtimes

Retrieves all check downtimes from updown.io.

```
GET https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-check-downtimes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a updown.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-check-downtimes?connectionId=$CONNECTION_ID&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-check-downtimes?${params}`, {
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
| `page` | number | no | The page to fetch, 100 per page. |
| `results` | boolean | no | Include detailed downtime results. |
| `token` | string | yes | The check unique token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details_url": "https://example.com",
      "duration": 1,
      "ended_at": "2026-05-07T12:00:00.000Z",
      "error": "string",
      "id": "string",
      "partial": true,
      "started_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details_url` | string | URL to the downtime details page. |
| `duration` | number | Downtime duration in seconds. |
| `ended_at` | date | Downtime end timestamp. |
| `error` | string | Error message for the downtime. |
| `id` | string | Downtime identifier. |
| `partial` | boolean | Whether the downtime record is partial. |
| `started_at` | date | Downtime start timestamp. |

## Native endpoint

Through the native updown.io API, this operation is `GET /checks/:token/downtimes` (base URL `https://updown.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-check-downtimes.md) for the provider-specific parameters and requirements.

