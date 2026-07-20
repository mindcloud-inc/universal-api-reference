# Loopy Loyalty: Create Subuser



```
POST https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-subuser
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-subuser" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "string",
  "username": "Ava Chen",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-subuser', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "string",
    "username": "Ava Chen",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | yes | Label for the sub-user for easy recognition. |
| `username` | string | yes | Subuser username. |
| `password` | string | yes | Subuser password. |

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
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created subuser ID. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /subuser` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subuser.md) for the provider-specific parameters and requirements.

