# Appwrite: Update Msg91 provider

Updates the Msg91 provider in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-update-msg91-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-update-msg91-provider" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "providerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-update-msg91-provider', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "providerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `providerId` | string | yes | Provider ID. |
| `name` | string | no | Provider name. |
| `enabled` | boolean | no | Set as enabled. |
| `templateId` | string | no | Msg91 template ID. |
| `senderId` | string | no | Msg91 sender ID. |
| `authKey` | string | no | Msg91 auth key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "credentials": {},
      "enabled": true,
      "name": "Ava Chen",
      "options": {},
      "provider": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Provider creation time in ISO 8601 format. |
| `$id` | string | Provider ID. |
| `$updatedAt` | string | Provider update date in ISO 8601 format. |
| `credentials` | object | Provider credentials. |
| `enabled` | boolean | Is provider enabled? |
| `name` | string | The name for the provider instance. |
| `options` | object | Provider options. |
| `provider` | string | The name of the provider service. |
| `type` | string | Type of provider. |

## Native endpoint

Through the native Appwrite API, this operation is `PATCH /messaging/providers/msg91/{providerId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/messaging-update-msg91-provider.md) for the provider-specific parameters and requirements.

