# LogRocket: Update User Information



```
PUT https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/update-user-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogRocket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/update-user-information" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/update-user-information', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The LogRocket user ID to create or update. |
| `name` | string | no | Optional user name. LogRocket allows up to 1024 characters. |
| `email` | string | no | Optional user email. LogRocket allows up to 1024 characters. Example: `user@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timestamp` | number | no | Optional Unix timestamp in milliseconds for the submitted user data. |
| `traits` | object | no | Optional object of user trait names and values. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "name": "Ava Chen",
      "traits": {},
      "userID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | User email |
| `name` | string | User name |
| `traits` | object | Stored user traits |
| `userID` | string | LogRocket user ID |

## Native endpoint

Through the native LogRocket API, this operation is `PUT /orgs/:orgId/apps/:projectId/users/:userId` (base URL `https://api.logrocket.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-information.md) for the provider-specific parameters and requirements.

