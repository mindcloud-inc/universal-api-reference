# Restoplace: Calculate Deposit

Calculates a deposit in Restoplace.

```
GET https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/calculate-deposit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restoplace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/calculate-deposit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/calculate-deposit?${params}`, {
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
| `from` | string | no | Reservation start date and time for the deposit calculation. |
| `to` | string | no | Reservation end date and time for the deposit calculation. |
| `count` | number | no | Number of guests for the deposit calculation. |
| `itemIds[]` | array<number> | no | Booking item IDs included in the deposit calculation. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `waitlist` | number | no | Whether the requested slot should be treated as a waitlist request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restoplace API returns.

## Native endpoint

Through the native Restoplace API, this operation is `POST /deposit/` (base URL `https://api.restoplace.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-deposit.md) for the provider-specific parameters and requirements.

