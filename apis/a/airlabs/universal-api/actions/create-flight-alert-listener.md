# Airlabs: Create Flight Alert Listener

Creates a flight alert listener in Airlabs.

```
POST https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/create-flight-alert-listener
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/create-flight-alert-listener" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/create-flight-alert-listener', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookUrl` | string | yes | Server URL to receive incoming flight alert webhook updates. |
| `flightNumber` | string | no | Listen for changes by flight number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `airlineIata` | string | no | Listen for changes by airline IATA code. |
| `airlineIcao` | string | no | Listen for changes by airline ICAO code. |
| `depIata` | string | no | Listen for changes by departure airport IATA code. |
| `depIcao` | string | no | Listen for changes by departure airport ICAO code. |
| `depDate` | date | no | Listen for changes by departure date. |
| `depTime` | string | no | Listen for changes by departure time. |
| `arrIata` | string | no | Listen for changes by arrival airport IATA code. |
| `arrIcao` | string | no | Listen for changes by arrival airport ICAO code. |
| `arrDate` | date | no | Listen for changes by arrival date. |
| `arrTime` | string | no | Listen for changes by arrival time. |
| `fields` | string | no | Comma-separated fields to listen for, or leave empty to listen for all changes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "listener_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `listener_id` | number | ID of the created listener. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /listen` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-flight-alert-listener.md) for the provider-specific parameters and requirements.

