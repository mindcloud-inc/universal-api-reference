# Mixpanel: Import Events

Creates new events in Mixpanel.

```
POST https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/import-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/import-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[].event": "string",
  "events[].properties.time": 1,
  "events[].properties.distinctId": "string",
  "events[].properties.insertId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/import-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[].event": "string",
    "events[].properties.time": 1,
    "events[].properties.distinctId": "string",
    "events[].properties.insertId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[].event` | string | yes | The event name for one imported event row. |
| `events[].properties.time` | number | yes | Event time in seconds or milliseconds since UTC epoch. |
| `events[].properties.distinctId` | string | yes | Distinct ID for the user who performed the event. |
| `events[].properties.insertId` | string | yes | Unique event identifier used for deduplication. |
| `events[].properties.extraProperties` | object | no | Additional custom event properties to merge into the event properties object. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `strict` | number | no | When 1, Mixpanel validates the batch and returns detailed errors for failed records. Default: `1`. |
| `projectId` | number | no | Required if using service account authentication for this request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "error": "string",
      "failedRecords": [
        {
          "field": "string",
          "index": 1,
          "insertId": "string",
          "message": "string"
        }
      ],
      "numRecordsImported": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | HTTP-style result code returned by Mixpanel. |
| `error` | string | Validation or transport error summary when the request fails. |
| `failedRecords` | array<object> | Per-record validation failures returned when strict validation fails. |
| `failedRecords[].field` | string | The field Mixpanel rejected for one failed record. |
| `failedRecords[].index` | number | Zero-based event index for one failed record. |
| `failedRecords[].insertId` | string | The failed record insert identifier when Mixpanel returns it. |
| `failedRecords[].message` | string | Validation message for one failed record. |
| `numRecordsImported` | number | Count of records Mixpanel ingested from the submitted batch. |
| `status` | string | High-level Mixpanel status string such as OK or Bad Request. |

## Native endpoint

Through the native Mixpanel API, this operation is `POST https://api.mixpanel.com/import` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-events.md) for the provider-specific parameters and requirements.

