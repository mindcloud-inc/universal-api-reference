# EMnify: Get Monthly Organization Traffic And Cost Statistics

Retrieves monthly organization traffic and cost statistics from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-monthly-organization-traffic-and-cost-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-monthly-organization-traffic-and-cost-statistics?connectionId=$CONNECTION_ID&authToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-monthly-organization-traffic-and-cost-statistics?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "prepaidBalance": {
        "amount": 1,
        "currency": {
          "code": "string",
          "id": 1,
          "symbol": "string"
        },
        "lastUpdate": "2026-05-07T12:00:00.000Z"
      },
      "serviceProfiles": 1,
      "sim": {
        "active": 1,
        "factoryTest": 1,
        "issued": 1,
        "suspended": 1,
        "total": 1
      },
      "tariffProfiles": 1,
      "users": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `prepaidBalance.amount` | number |  |
| `prepaidBalance.currency.code` | string |  |
| `prepaidBalance.currency.id` | number |  |
| `prepaidBalance.currency.symbol` | string |  |
| `prepaidBalance.lastUpdate` | date |  |
| `serviceProfiles` | number |  |
| `sim.active` | number |  |
| `sim.factoryTest` | number |  |
| `sim.issued` | number |  |
| `sim.suspended` | number |  |
| `sim.total` | number |  |
| `tariffProfiles` | number |  |
| `users` | number |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /organisation/:org_id_or_my/stats` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monthly-organization-traffic-and-cost-statistics.md) for the provider-specific parameters and requirements.

