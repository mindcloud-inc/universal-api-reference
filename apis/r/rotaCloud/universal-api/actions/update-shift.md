# RotaCloud: Update Shift

Updates a shift in RotaCloud.

```
PUT https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-shift" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-shift', {
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
| `id` | number | yes | Shift ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "end_time": 1,
      "id": 1,
      "location": 1,
      "notes": "string",
      "open": true,
      "published": true,
      "role": 1,
      "start_time": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `end_time` | number |  |
| `id` | number |  |
| `location` | number |  |
| `notes` | string |  |
| `open` | boolean |  |
| `published` | boolean |  |
| `role` | number |  |
| `start_time` | number |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/shifts/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shift.md) for the provider-specific parameters and requirements.

