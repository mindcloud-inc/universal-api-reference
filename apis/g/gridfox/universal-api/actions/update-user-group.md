# Gridfox: Update User Group

Updates a user's group in a Gridfox project.

```
PUT https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/update-user-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridfox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/update-user-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/update-user-group', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupName` | string | no | Name of the Gridfox group to assign the user to. |
| `userId` | string | no | Numeric Gridfox user ID from the path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the user group update succeeded. |

## Native endpoint

Through the native Gridfox API, this operation is `PUT /users/:userId` (base URL `https://api.gridfox.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-group.md) for the provider-specific parameters and requirements.

