# Magileads: Create PRM Custom Status

Creates a new PRM custom status in Magileads.

```
POST https://connect.mindcloud.co/v1/universal/magileads/latest/actions/create-prm-custom-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Magileads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/create-prm-custom-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/magileads/latest/actions/create-prm-custom-status', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The custom status name. |
| `color` | string | no | The custom status color in hex. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "state": true,
      "status_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `state` | boolean |  |
| `status_id` | number |  |

## Native endpoint

Through the native Magileads API, this operation is `POST /prm/status/custom` (base URL `https://app.api-magileads.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-prm-custom-status.md) for the provider-specific parameters and requirements.

