# Appwrite: Create SMTP provider

Creates a new SMTP provider in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-create-smtp-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-create-smtp-provider" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "providerId": "string",
  "name": "Ava Chen",
  "host": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-create-smtp-provider', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "providerId": "string",
    "name": "Ava Chen",
    "host": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `providerId` | string | yes | Provider ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | string | yes | Provider name. |
| `host` | string | yes | SMTP hosts. Either a single hostname or multiple semicolon-delimited hostnames. You can also specify a different port for each host such as `smtp1.example.com:25;smtp2.example.com`. You can also specify encryption type, for example: `tls://smtp1.example.com:587;ssl://smtp2.example.com:465"`. Hosts will be tried in order. |
| `port` | number | no | The default SMTP server port. |
| `username` | string | no | Authentication username. |
| `password` | string | no | Authentication password. |
| `encryption` | string | no | Encryption type. Can be omitted, 'ssl', or 'tls' |
| `autoTLS` | boolean | no | Enable SMTP AutoTLS feature. |
| `mailer` | string | no | The value to use for the X-Mailer header. |
| `fromName` | string | no | Sender Name. |
| `fromEmail` | string | no | Sender email address. |
| `replyToName` | string | no | Name set in the reply to field for the mail. Default value is sender name. |
| `replyToEmail` | string | no | Email set in the reply to field for the mail. Default value is sender email. |
| `enabled` | boolean | no | Set as enabled. |

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

Through the native Appwrite API, this operation is `POST /messaging/providers/smtp` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/messaging-create-smtp-provider.md) for the provider-specific parameters and requirements.

