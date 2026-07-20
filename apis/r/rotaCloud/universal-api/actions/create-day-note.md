# RotaCloud: Create Day Note

Creates a day note in RotaCloud.

```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-day-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-day-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "start_date": "string",
  "end_date": "string",
  "locations[]": [
    1
  ],
  "title": "string",
  "message": "string",
  "visible_employees": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-day-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "start_date": "string",
    "end_date": "string",
    "locations[]": [1],
    "title": "string",
    "message": "string",
    "visible_employees": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start_date` | string | yes | Day note start date in YYYY-MM-DD format. |
| `end_date` | string | yes | Day note end date in YYYY-MM-DD format. |
| `locations[]` | array<number> | yes | Location IDs affected by the day note. |
| `title` | string | yes | Day note title. |
| `message` | string | yes | Day note body text. |
| `visible_employees` | boolean | yes | Whether employees can see the day note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end_date": "string",
      "id": 1,
      "locations": [
        1
      ],
      "message": "string",
      "start_date": "string",
      "title": "string",
      "visible_employees": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end_date` | string |  |
| `id` | number |  |
| `locations` | array<number> |  |
| `message` | string |  |
| `start_date` | string |  |
| `title` | string |  |
| `visible_employees` | boolean |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/day_notes` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-day-note.md) for the provider-specific parameters and requirements.

