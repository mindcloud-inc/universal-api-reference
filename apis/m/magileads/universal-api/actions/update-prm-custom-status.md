# Magileads: Update PRM Custom Status

Updates an existing PRM custom status in Magileads.

```
PUT https://connect.mindcloud.co/v1/universal/magileads/latest/actions/update-prm-custom-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Magileads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/update-prm-custom-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "status_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/magileads/latest/actions/update-prm-custom-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "status_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | string | no | The updated custom status color in hex. |
| `name` | string | no | The updated custom status name. |
| `status_id` | number | yes | The custom status ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "state": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `state` | boolean |  |

## Native endpoint

Through the native Magileads API, this operation is `PUT /prm/status/custom/:status_id` (base URL `https://app.api-magileads.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-prm-custom-status.md) for the provider-specific parameters and requirements.

