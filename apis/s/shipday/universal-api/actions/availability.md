# Shipday: Availability

Checks on-demand service availability in Shipday.

```
GET https://connect.mindcloud.co/v1/universal/shipday/latest/actions/availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/availability?connectionId=$CONNECTION_ID&pickupAddress=1%20Wall%20St%2C%20New%20York%2C%20NY%2010005%2C%20USA&deliveryAddress=1000%205th%20Ave%2C%20New%20York%2C%20NY%2010028%2C%20USA&deliveryTime=2025-06-25T17%3A20%3A26Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pickupAddress": "1 Wall St, New York, NY 10005, USA",
  "deliveryAddress": "1000 5th Ave, New York, NY 10028, USA",
  "deliveryTime": "2025-06-25T17:20:26Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipday/latest/actions/availability?${params}`, {
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
| `pickupAddress` | string | yes | Pickup address used for on-demand availability lookup. Example: `1 Wall St, New York, NY 10005, USA`. |
| `deliveryAddress` | string | yes | Delivery address used for on-demand availability lookup. Example: `1000 5th Ave, New York, NY 10028, USA`. |
| `deliveryTime` | date | yes | Requested delivery timestamp for the availability check. Example: `2025-06-25T17:20:26Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryDuration": 1,
      "deliveryTime": "2026-05-07T12:00:00.000Z",
      "error": true,
      "errorCode": "string",
      "errorDescription": "string",
      "errorMessage": "string",
      "fee": 1,
      "id": "string",
      "isInternal": true,
      "isProd": true,
      "name": "Ava Chen",
      "pickupDuration": 1,
      "pickupTime": "2026-05-07T12:00:00.000Z",
      "probableAssignment": true,
      "regulatoryFee": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryDuration` | number | Estimated delivery duration in minutes. |
| `deliveryTime` | date | Estimated delivery timestamp. |
| `error` | boolean | Whether the provider returned an error. |
| `errorCode` | string | Provider error code when present. |
| `errorDescription` | string | Provider error description when present. |
| `errorMessage` | string | Provider error message when present. |
| `fee` | number | Quoted delivery fee. |
| `id` | string | Provider identifier for the availability row. |
| `isInternal` | boolean | Whether the provider route is internal. |
| `isProd` | boolean | Whether the quote came from a production provider configuration. |
| `name` | string | Provider name. |
| `pickupDuration` | number | Estimated pickup duration in minutes. |
| `pickupTime` | date | Estimated pickup timestamp. |
| `probableAssignment` | boolean | Whether the provider indicates likely assignment. |
| `regulatoryFee` | number | Additional regulatory fee when present. |

## Native endpoint

Through the native Shipday API, this operation is `POST /on-demand/availability` (base URL `https://api.shipday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/availability.md) for the provider-specific parameters and requirements.

