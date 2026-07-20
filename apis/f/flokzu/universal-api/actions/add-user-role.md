# Flokzu: Add User Role



```
PUT https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/add-user-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flokzu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/add-user-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/add-user-role', {
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
      "detail": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detail` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Flokzu API, this operation is `POST /v1/management/user/roles` (base URL `https://app.flokzu.com/flokzuopenapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-role.md) for the provider-specific parameters and requirements.

