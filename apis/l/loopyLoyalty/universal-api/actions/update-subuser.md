# Loopy Loyalty: Update Subuser



```
PUT https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/update-subuser
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/update-subuser" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/update-subuser', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Subuser ID. |
| `label` | string | no | Label for the sub-user for easy recognition. |
| `username` | string | no | Subuser username. |
| `password` | string | no | Subuser password. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | Subuser status. |
| `location.id` | string | no | Subuser location ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "string",
      "id": "string",
      "label": "string",
      "location": {
        "id": "string",
        "name": "Ava Chen"
      },
      "parent": "string",
      "status": "string",
      "updateTime": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | string | Creation timestamp. |
| `id` | string | Subuser ID. |
| `label` | string | Subuser label. |
| `location.id` | string | Assigned location ID. |
| `location.name` | string | Assigned location name. |
| `parent` | string | Parent user ID. |
| `status` | string | Subuser status. |
| `updateTime` | string | Last update timestamp. |
| `username` | string | Subuser username. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `PATCH /subuser/:id` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subuser.md) for the provider-specific parameters and requirements.

