# GIRITON: List Shifts

Retrieves a list of shifts from GIRITON.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-shifts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-shifts?${params}`, {
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
| `validSince` | string | no | Valid since date for shifts. |
| `validUntil` | string | no | Valid until date for shifts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "breakDuration": "string",
      "color": "string",
      "departments": [
        {}
      ],
      "endsAt": "string",
      "entryTimestamp": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "overtimeTresholdDuration": "string",
      "shortcut": "string",
      "startsAt": "string",
      "tags": [
        "string"
      ],
      "validSince": "2026-05-07T12:00:00.000Z",
      "validUntil": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breakDuration` | string | Break duration. |
| `color` | string | Shift color. |
| `departments` | array<object> | Associated departments. |
| `endsAt` | string | Shift end time. |
| `entryTimestamp` | date | Shift entry timestamp. |
| `id` | string | Shift ID. |
| `name` | string | Shift name. |
| `overtimeTresholdDuration` | string | Overtime threshold duration. |
| `shortcut` | string | Shift shortcut. |
| `startsAt` | string | Shift start time. |
| `tags` | array<string> | Shift tags. |
| `validSince` | date | Date from which the shift is valid. |
| `validUntil` | date | Date until which the shift is valid. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /shift/shifts` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shifts.md) for the provider-specific parameters and requirements.

