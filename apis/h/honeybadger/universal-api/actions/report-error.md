# Honeybadger: Report Error

Reports an application error to Honeybadger.

```
POST https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/report-error
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Honeybadger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/report-error" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "error.class": "string",
  "error.message": "string",
  "error.backtrace[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/report-error', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "error.class": "string",
    "error.message": "string",
    "error.backtrace[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notifier.name` | string | no | Name of the notifier sending the Honeybadger error report. |
| `notifier.url` | string | no | URL for the notifier package or integration. |
| `notifier.version` | string | no | Version of the notifier package or integration. |
| `error.class` | string | yes | Error class or exception type. |
| `error.message` | string | yes | Human-readable error message. |
| `error.backtrace[]` | array<object> | yes | Ruby-style backtrace frames for grouping and error inspection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Honeybadger notice identifier returned after a successful error report. |

## Native endpoint

Through the native Honeybadger API, this operation is `POST /notices` (base URL `https://api.honeybadger.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/report-error.md) for the provider-specific parameters and requirements.

