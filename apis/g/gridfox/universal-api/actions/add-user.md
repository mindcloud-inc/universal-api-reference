# Gridfox: Add User

Adds a user to a Gridfox project.

```
POST https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/add-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridfox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/add-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/add-user', {
  method: 'POST',
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
| `email` | string | no | Email address of the user to add to the project. |
| `groupName` | string | no | Name of the Gridfox group to assign the added user to. |

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
| `success` | boolean | Whether the user invitation succeeded. |

## Native endpoint

Through the native Gridfox API, this operation is `POST /users` (base URL `https://api.gridfox.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user.md) for the provider-specific parameters and requirements.

