# Sharetribe: Create Availability Exceptions

Creates new availability exceptions in Sharetribe.

```
POST https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/create-availability-exceptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sharetribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/create-availability-exceptions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listingId": "string",
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z",
  "seats": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/create-availability-exceptions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listingId": "string",
    "start": "2026-05-07T12:00:00.000Z",
    "end": "2026-05-07T12:00:00.000Z",
    "seats": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listingId` | string | yes | The listing ID. |
| `start` | date | yes | Availability exception interval start time in ISO 8601 format. |
| `end` | date | yes | Availability exception interval end time in ISO 8601 format. |
| `seats` | number | yes | Number of available seats for the given range. Set to 0 to block the range. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Resource attributes payload. |
| `id` | string | Resource ID. |
| `relationships` | object | Resource relationships payload. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Sharetribe API, this operation is `POST availability_exceptions/create` (base URL `https://flex-integ-api.sharetribe.com/v1/integration_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-availability-exceptions.md) for the provider-specific parameters and requirements.

