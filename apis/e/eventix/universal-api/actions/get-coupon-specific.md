# Eventix: Get a specific Coupon

Retrieves a specific coupon from Eventix.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-coupon-specific
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-coupon-specific?connectionId=$CONNECTION_ID&guid=coupon-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "coupon-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-coupon-specific?${params}`, {
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
| `guid` | string | yes | The guid of the Coupon. Example: `coupon-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "description": "string",
      "end_date": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "note": "string",
      "start_date": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `description` | string |  |
| `end_date` | date |  |
| `name` | string |  |
| `note` | string |  |
| `start_date` | date |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/coupon/:guid` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coupon-specific.md) for the provider-specific parameters and requirements.

