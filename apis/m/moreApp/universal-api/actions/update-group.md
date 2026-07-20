# MoreApp: Update Group

Updates a group in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "209321",
  "groupId": "69bc4c7a0e76586ace7d82bd",
  "name": "MindCloud Temp Group Updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "209321",
    "groupId": "69bc4c7a0e76586ace7d82bd",
    "name": "MindCloud Temp Group Updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `groupId` | string | yes | MoreApp group identifier. Default: `69bc4c7a0e76586ace7d82bd`. |
| `name` | string | yes | Updated group name. Default: `MindCloud Temp Group Updated`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externallyManaged": true,
      "grants": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externallyManaged` | boolean |  |
| `grants` | array<object> |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `PATCH /api/v2/customers/{{customerId}}/groups/{{groupId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

