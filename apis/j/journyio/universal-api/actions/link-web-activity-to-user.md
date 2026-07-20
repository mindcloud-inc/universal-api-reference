# Journy.io: Link Web Activity to User



```
POST https://connect.mindcloud.co/v1/universal/journyio/latest/actions/link-web-activity-to-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Journy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/journyio/latest/actions/link-web-activity-to-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deviceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/journyio/latest/actions/link-web-activity-to-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deviceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceId` | string | yes | Value of the __journey cookie to link. |
| `identification.email` | string | no | Email address of the user. |
| `identification.userId` | string | no | Unique identifier for the user in your database. |

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
      }
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

## Native endpoint

Through the native Journy.io API, this operation is `POST /link` (base URL `https://api.journy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/link-web-activity-to-user.md) for the provider-specific parameters and requirements.

