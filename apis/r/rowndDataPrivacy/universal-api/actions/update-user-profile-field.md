# Rownd Data Privacy: Update User Profile Field



```
PUT https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/update-user-profile-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/update-user-profile-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "field": "string",
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/update-user-profile-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "field": "string",
    "user": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `field` | string | yes | User-profile field name. |
| `user` | string | yes | Rownd user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Updated field value when returned. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `PUT /users/:user/data/fields/:field` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-profile-field.md) for the provider-specific parameters and requirements.

