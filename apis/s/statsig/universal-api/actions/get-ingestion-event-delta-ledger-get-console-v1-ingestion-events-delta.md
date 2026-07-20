# Statsig: Get Ingestion Event Delta Ledger

Retrieves an ingestion event delta ledger from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-ingestion-event-delta-ledger-get-console-v1-ingestion-events-delta
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-ingestion-event-delta-ledger-get-console-v1-ingestion-events-delta?connectionId=$CONNECTION_ID&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-ingestion-event-delta-ledger-get-console-v1-ingestion-events-delta?${params}`, {
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
| `startDate` | string | yes | Expected valid date in the form of YYYY-MM-DD |
| `endDate` | string | yes | Expected valid date in the form of YYYY-MM-DD |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceName` | string | no |  |
| `eventName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `GET /console/v1/ingestion/events/delta` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ingestion-event-delta-ledger-get-console-v1-ingestion-events-delta.md) for the provider-specific parameters and requirements.

