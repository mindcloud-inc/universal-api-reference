# Sonderplan: Get Booking Clashes



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-booking-clashes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-booking-clashes?connectionId=$CONNECTION_ID&end=string&start=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "string",
  "start": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-booking-clashes?${params}`, {
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
| `end` | string | yes | End datetime for clash checking. |
| `start` | string | yes | Start datetime for clash checking. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": 1,
      "id": 1,
      "name": "Ava Chen",
      "start": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | number |  |
| `id` | number |  |
| `name` | string |  |
| `start` | number |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /booking/checkclash` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking-clashes.md) for the provider-specific parameters and requirements.

