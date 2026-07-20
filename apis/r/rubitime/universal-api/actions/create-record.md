# Rubitime: Create Record

Creates a new record in Rubitime.

```
POST https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rubitime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "branchId": 1,
  "cooperatorId": 1,
  "serviceId": 1,
  "record": "2026-05-01 10:00:00",
  "status": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "branchId": 1,
    "cooperatorId": 1,
    "serviceId": 1,
    "record": "2026-05-01 10:00:00",
    "status": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branchId` | number | yes | Rubitime branch ID. |
| `cooperatorId` | number | yes | Rubitime employee/cooperator ID. |
| `serviceId` | number | yes | Rubitime service ID. |
| `record` | string | yes | Appointment date and time, for example 2021-12-08 13:30:03. Example: `2026-05-01 10:00:00`. |
| `status` | number | yes | Record status code documented by Rubitime. Default: `0`. |
| `name` | string | no | Customer full name. |
| `email` | string | no | Customer email address. |
| `phone` | string | no | Customer phone number. |
| `comment` | string | no | Customer comment for the record. |
| `price` | number | no | Service price. |
| `duration` | number | no | Service duration in minutes. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prepayment` | number | no | Prepayment amount. |
| `prepaymentDate` | string | no | Prepayment completion date and time. Example: `2026-05-01 09:00:00`. |
| `prepaymentUrl` | string | no | Prepayment URL. |
| `reminderMinutes` | number | no | Reminder offset in minutes. |
| `reminder` | string | no | Optional reminder timestamp documented by Rubitime. Example: `2035-01-01 09:00:00`. |
| `whom` | number | no | Creator marker; 0 means customer, other values indicate administrator. |
| `source` | string | no | Record source. Rubitime defaults this to api. |
| `customField1` | string | no | First Rubitime custom field value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Record ID returned by Rubitime. |
| `url` | string | Rubitime record URL returned by the create-record endpoint. |

## Native endpoint

Through the native Rubitime API, this operation is `POST /create-record` (base URL `https://rubitime.ru/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

