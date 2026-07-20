# OneSignal: Update User

Updates an existing user in OneSignal.

```
PUT https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "aliasId": "string",
  "aliasLabel": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "aliasId": "string",
    "aliasLabel": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aliasId` | string | yes | The alias value for the selected alias label. |
| `aliasLabel` | string | yes | The alias namespace to look up, such as external_id. |
| `properties` | object | no | An object of user properties to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "properties": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `properties` | object | The updated user properties returned by OneSignal. |

## Native endpoint

Through the native OneSignal API, this operation is `PATCH /apps/:app_id/users/by/:alias_label/:alias_id` (base URL `https://api.onesignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

