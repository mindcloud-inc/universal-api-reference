# Monta: List Charges

Retrieves charges from Monta.

```
GET https://connect.mindcloud.co/v1/universal/monta/latest/actions/list-charges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monta `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/list-charges?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monta/latest/actions/list-charges?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chargePointId` | number | no | Only return charges for this charge point ID. |
| `state` | list<string> | no | Only return charges in this state. One of: `charging`, `completed`, `paused`, `reserved`, `scheduled`, `starting`, `stopped`, `stopping`. |
| `fromDate` | date | no | Only return charges created at or after this ISO 8601 date-time. Example: `2022-05-22T09:30:03Z`. |
| `toDate` | date | no | Only return charges created at or before this ISO 8601 date-time. Example: `2022-05-22T09:30:03Z`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averagePricePerKwh` | number |  |
| `cablePluggedInAt` | date |  |
| `chargePointId` | number |  |
| `consumedKwh` | number |  |
| `cost` | number |  |
| `createdAt` | date |  |
| `currency.decimals` | number |  |
| `currency.identifier` | string |  |
| `currency.name` | string |  |
| `failedAt` | date |  |
| `failureReason` | string |  |
| `fullyChargedAt` | date |  |
| `humanReadableId` | string |  |
| `id` | number |  |
| `kwhLimit` | number |  |
| `note` | string |  |
| `price` | number |  |
| `priceLimit` | number |  |
| `soc.percentage` | number |  |
| `soc.source` | string |  |
| `socLimit` | number |  |
| `startedAt` | date |  |
| `state` | string |  |
| `stoppedAt` | date |  |
| `stopReason` | string |  |
| `timeoutAt` | date |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Monta API, this operation is `GET /charges` (base URL `https://public-api.monta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-charges.md) for the provider-specific parameters and requirements.

