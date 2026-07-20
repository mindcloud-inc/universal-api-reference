# Monta Universal API Examples

These examples use the MindCloud API key and Monta connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Application

Retrieves the current application from Monta.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-current-application?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-current-application?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "scopes": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Current Application action reference](actions/get-current-application.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/monta/latest/actions/get-current-application).

## Start Charge

Starts a new charge in Monta.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/monta/latest/actions/start-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chargePointId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monta/latest/actions/start-charge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chargePointId": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "averagePricePerKwh": 1,
      "cablePluggedInAt": "2026-05-07T12:00:00.000Z",
      "chargePointId": 1,
      "consumedKwh": 1,
      "cost": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": {
        "decimals": 1,
        "identifier": "string",
        "name": "Ava Chen"
      },
      "failedAt": "2026-05-07T12:00:00.000Z",
      "failureReason": "string",
      "fullyChargedAt": "2026-05-07T12:00:00.000Z",
      "humanReadableId": "string",
      "id": 1,
      "kwhLimit": 1,
      "note": "string",
      "price": 1,
      "priceLimit": 1,
      "soc": {
        "percentage": 1,
        "source": "string"
      },
      "socLimit": 1,
      "startedAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "stoppedAt": "2026-05-07T12:00:00.000Z",
      "stopReason": "string",
      "timeoutAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Start Charge action reference](actions/start-charge.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/monta/latest/actions/start-charge).
