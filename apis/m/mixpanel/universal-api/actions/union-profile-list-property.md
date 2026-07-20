# Mixpanel: Union Profile List Property

Unions values into a user profile list in Mixpanel.

```
PUT https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/union-profile-list-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/union-profile-list-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "distinctId": "user_123",
  "union": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/union-profile-list-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "distinctId": "user_123",
    "union": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `distinctId` | string | yes | Distinct ID of the user profile to update. Example: `user_123`. |
| `union` | object | yes | Object mapping profile list properties to values that should be unioned. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ip` | number | no | Set to 1 to use the request IP for geolocation updates. Example: `1`. |
| `strict` | number | no | Set to 1 to return validation errors for invalid updates. Example: `1`. |
| `verbose` | number | no | Set to 1 to include verbose validation messages in the response. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | number | Mixpanel ingestion success flag where 1 indicates success and 0 indicates failure. |

## Native endpoint

Through the native Mixpanel API, this operation is `POST https://api.mixpanel.com/engage` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/union-profile-list-property.md) for the provider-specific parameters and requirements.

