# Next Cloud OCS: Add User To Group

Adds a user to a group in Next Cloud OCS.

```
POST https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/add-user-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/add-user-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/add-user-to-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | Group ID to add the user to. |
| `userId` | string | yes | Nextcloud user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": "string",
      "statuscode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | string |  |
| `statuscode` | number |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `POST /ocs/v1.php/cloud/users/{{userId}}/groups` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-group.md) for the provider-specific parameters and requirements.

