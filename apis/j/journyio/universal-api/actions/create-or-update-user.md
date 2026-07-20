# Journy.io: Create or Update User



```
PUT https://connect.mindcloud.co/v1/universal/journyio/latest/actions/create-or-update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Journy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/journyio/latest/actions/create-or-update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/journyio/latest/actions/create-or-update-user', {
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
| `identification.email` | string | no | Email address of the user. |
| `identification.userId` | string | no | Unique identifier for the user in your database. |
| `properties` | object | no | User properties to create or update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "meta": {
        "requestId": "string",
        "status": 1
      },
      "rejected": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `meta.requestId` | string |  |
| `meta.status` | number |  |
| `rejected` | object |  |

## Native endpoint

Through the native Journy.io API, this operation is `POST /users/upsert` (base URL `https://api.journy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-user.md) for the provider-specific parameters and requirements.

