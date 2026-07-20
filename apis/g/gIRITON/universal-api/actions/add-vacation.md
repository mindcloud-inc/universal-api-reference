# GIRITON: Add Vacation

Creates a new vacation entry in GIRITON.

```
POST https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/add-vacation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/add-vacation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dateFrom": "string",
  "dateTo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/add-vacation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dateFrom": "string",
    "dateTo": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateFrom` | string | yes | Starting date of vacation. |
| `userEmail` | string | no | User email address for the vacation. |
| `userId` | string | no | User ID for the vacation. |
| `userNumber` | string | no | User number for the vacation. |
| `dateTo` | string | yes | Last date of vacation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "entries": [
        {}
      ],
      "newestTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of returned vacation entries. |
| `entries` | array<object> | Vacation records. |
| `newestTimestamp` | date | Newest entry timestamp. |

## Native endpoint

Through the native GIRITON API, this operation is `POST /attendance/vacation` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-vacation.md) for the provider-specific parameters and requirements.

