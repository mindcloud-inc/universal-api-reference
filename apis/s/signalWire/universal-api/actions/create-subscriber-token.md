# SignalWire: Create Subscriber Token

Creates a new subscriber token in SignalWire.

```
POST https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-subscriber-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-subscriber-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reference": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-subscriber-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reference": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reference` | string | yes | A string that uniquely identifies the subscriber. Often it's an email, but can be any other string. |
| `expireAt` | number | no | A unixtime (the number of seconds since 1970-01-01 00:00:00) at which the token should no longer be valid. Defaults to 'two hours from now' |
| `applicationId` | string | no | The ID of the application that the token is associated with. |
| `password` | string | no | Set or update the subscriber's password. Omit this field or pass an empty string if you don't want to update the password. |
| `firstName` | string | no | Set or update the first name of the subscriber. |
| `lastName` | string | no | Set or update the last name of the subscriber. |
| `displayName` | string | no | Set or update the display name of the subscriber. |
| `jobTitle` | string | no | Set or update the job title of the subscriber. |
| `timeZone` | string | no | Set or update the time zone of the subscriber. |
| `country` | string | no | Set or update the country of the subscriber. |
| `region` | string | no | Set or update the region of the subscriber. |
| `companyName` | string | no | Set or update the company name of the subscriber. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "refresh_token": "string",
      "subscriber_id": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `refresh_token` | string | Refresh token. |
| `subscriber_id` | string | The ID of the subscriber that the token is associated with. |
| `token` | string | The token that is associated with the subscriber. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /fabric/subscribers/tokens` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscriber-token.md) for the provider-specific parameters and requirements.

