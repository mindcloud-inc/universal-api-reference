# Headless Testing: Update User Info

Updates user information in Headless Testing.

```
PUT https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-user-info" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-user-info', {
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
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "plan": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `first_name` | string |  |
| `id` | number |  |
| `last_name` | string |  |
| `plan` | string |  |

## Native endpoint

Through the native Headless Testing API, this operation is `PUT /user` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-info.md) for the provider-specific parameters and requirements.

