# RotaCloud: Update Day Note V2



```
PUT https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-day-note-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-day-note-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "startDate": "string",
  "endDate": "string",
  "locations[]": [
    1
  ],
  "title": "string",
  "message": "string",
  "visibleToEmployees": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-day-note-v2', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "startDate": "string",
    "endDate": "string",
    "locations[]": [1],
    "title": "string",
    "message": "string",
    "visibleToEmployees": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Day note ID. |
| `startDate` | string | yes | Day note start date in YYYY-MM-DD format. |
| `endDate` | string | yes | Day note end date in YYYY-MM-DD format. |
| `locations[]` | array<number> | yes | Location IDs affected by the day note. |
| `title` | string | yes | Day note title. |
| `message` | string | yes | Day note body text. |
| `visibleToEmployees` | boolean | yes | Whether employees can see the day note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedAt": "string",
      "addedBy": 1,
      "endDate": "string",
      "id": 1,
      "locations": [
        1
      ],
      "message": "string",
      "startDate": "string",
      "title": "string",
      "updatedAt": "string",
      "updatedBy": 1,
      "visibleToEmployees": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedAt` | string |  |
| `addedBy` | number |  |
| `endDate` | string |  |
| `id` | number |  |
| `locations` | array<number> |  |
| `message` | string |  |
| `startDate` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `updatedBy` | number |  |
| `visibleToEmployees` | boolean |  |

## Native endpoint

Through the native RotaCloud API, this operation is `PUT /v2/dayNotes/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-day-note-v2.md) for the provider-specific parameters and requirements.

