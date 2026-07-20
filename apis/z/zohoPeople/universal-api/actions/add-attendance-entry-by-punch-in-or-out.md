# Zoho People: Add Attendance Entry by Punch In or Out

Creates attendance entries by punch direction in Zoho People.

```
POST https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/add-attendance-entry-by-punch-in-or-out
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/add-attendance-entry-by-punch-in-or-out" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "direction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/add-attendance-entry-by-punch-in-or-out', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "direction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `direction` | string | yes | Punch direction. Use in or out. |
| `latitude` | string | no | Latitude of the punch location. Zoho documents this parameter as lattitude. |
| `longitude` | string | no | Longitude of the punch location. |
| `accuracy` | string | no | Accuracy of the punch location. |
| `description` | string | no | Optional description to attach to the punch event. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho People API, this operation is `POST /api/v3/attendance/entries/:direction` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-attendance-entry-by-punch-in-or-out.md) for the provider-specific parameters and requirements.

