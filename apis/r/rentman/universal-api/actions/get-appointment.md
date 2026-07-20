# Rentman: Get Appointment



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-appointment?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-appointment?${params}`, {
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
| `id` | number | yes | Numeric Rentman appointment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "displayname": "Ava Chen",
      "end": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_plannable": true,
      "is_public": true,
      "location": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "recurrence_enddate": "2026-05-07T12:00:00.000Z",
      "recurrence_group": 1,
      "recurrence_interval": 1,
      "recurrence_interval_unit": "string",
      "recurrence_weekdays": "string",
      "remark": "string",
      "start": "2026-05-07T12:00:00.000Z",
      "synchronisation_uri": "string",
      "synchronization_id": "string",
      "updateHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created` | date |  |
| `creator` | string |  |
| `displayname` | string |  |
| `end` | date |  |
| `id` | number |  |
| `is_plannable` | boolean |  |
| `is_public` | boolean |  |
| `location` | string |  |
| `modified` | date |  |
| `name` | string |  |
| `recurrence_enddate` | date |  |
| `recurrence_group` | number |  |
| `recurrence_interval` | number |  |
| `recurrence_interval_unit` | string |  |
| `recurrence_weekdays` | string |  |
| `remark` | string |  |
| `start` | date |  |
| `synchronisation_uri` | string |  |
| `synchronization_id` | string |  |
| `updateHash` | string |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /appointments/:id` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-appointment.md) for the provider-specific parameters and requirements.

