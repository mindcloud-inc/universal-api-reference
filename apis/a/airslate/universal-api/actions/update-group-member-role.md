# Airslate: Update Group Member Role

Updates a group member role in airSlate.

```
PUT https://connect.mindcloud.co/v1/universal/airslate/latest/actions/update-group-member-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airslate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airslate/latest/actions/update-group-member-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airslate/latest/actions/update-group-member-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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
| `id` | string |  |

## Native endpoint

Through the native Airslate API, this operation is `PATCH /organizations/{organization_id}/groups/{group_id}/members/{user_id}` (base URL `https://api.airslate.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group-member-role.md) for the provider-specific parameters and requirements.

