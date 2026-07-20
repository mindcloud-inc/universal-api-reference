# Statsig: Backfill Ingestion

Backfills an ingestion in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/backfill-ingestion-post-console-v1-ingestion-backfill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/backfill-ingestion-post-console-v1-ingestion-backfill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datestampStart": "string",
  "datestampEnd": "string",
  "type": "string",
  "dataset": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/backfill-ingestion-post-console-v1-ingestion-backfill', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datestampStart": "string",
    "datestampEnd": "string",
    "type": "string",
    "dataset": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datestampStart` | string | yes | Request body field. |
| `datestampEnd` | string | yes | Request body field. |
| `type` | string | yes | Request body field. |
| `source` | string | no | Request body field. |
| `dataset` | string | yes | Request body field. |

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

Through the native Statsig API, this operation is `POST /console/v1/ingestion/backfill` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/backfill-ingestion-post-console-v1-ingestion-backfill.md) for the provider-specific parameters and requirements.

