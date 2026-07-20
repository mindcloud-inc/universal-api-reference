# OTO: List Available Time Slots

Retrieves available time slots from the OTO API.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-available-time-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-available-time-slots?connectionId=$CONNECTION_ID&serviceType=string&packageSize=string&lat=string&lon=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serviceType": "string",
  "packageSize": "string",
  "lat": "string",
  "lon": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-available-time-slots?${params}`, {
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
| `serviceType` | string | yes | Service type to price or schedule, for example bullet. |
| `packageSize` | string | yes | Package size token used by OTO, for example simCard. |
| `lat` | string | yes | Pickup latitude. |
| `lon` | string | yes | Pickup longitude. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableSlots": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableSlots` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native OTO API, this operation is `POST /availableTimeslots` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-time-slots.md) for the provider-specific parameters and requirements.

