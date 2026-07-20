# Magileads: Update PRM Nurturing

Updates an existing PRM nurturing in Magileads.

```
PUT https://connect.mindcloud.co/v1/universal/magileads/latest/actions/update-prm-nurturing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Magileads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/update-prm-nurturing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nurturing_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/magileads/latest/actions/update-prm-nurturing', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nurturing_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The updated nurturing name. |
| `nurturing_id` | number | yes | The nurturing ID. |
| `filter` | object | no | The updated nurturing filter object. |
| `contactListIds[]` | array<number> | no | The updated contact list IDs. |

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

Through the native Magileads API, this operation is `PUT /prm/nurturing/:nurturing_id` (base URL `https://app.api-magileads.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-prm-nurturing.md) for the provider-specific parameters and requirements.

