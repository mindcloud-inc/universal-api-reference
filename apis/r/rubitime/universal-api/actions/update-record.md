# Rubitime: Update Record

Updates an existing record in Rubitime.

```
PUT https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rubitime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Rubitime record ID to update. |
| `branchId` | number | no | Rubitime branch ID. |
| `cooperatorId` | number | no | Rubitime employee/cooperator ID. |
| `serviceId` | number | no | Rubitime service ID. |
| `record` | string | no | Appointment date and time. Example: `2026-05-01 10:00:00`. |
| `status` | number | no | Record status code documented by Rubitime. |
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
| `source` | string | no | Record source. |
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
| `url` | string | Rubitime record URL returned by the record endpoint. |

## Native endpoint

Through the native Rubitime API, this operation is `POST /update-record` (base URL `https://rubitime.ru/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.

