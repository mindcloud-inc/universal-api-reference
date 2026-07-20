# RingCentral: Send SMS

Sends an SMS message from a RingCentral extension.

```
POST https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RingCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "extensionId": "string",
  "from.phoneNumber": "string",
  "to.phoneNumber[]": [
    "string"
  ],
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "extensionId": "string",
    "from.phoneNumber": "string",
    "to.phoneNumber[]": ["string"],
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes |  |
| `extensionId` | string | yes |  |
| `from.phoneNumber` | string | yes |  |
| `to.phoneNumber[]` | array<string> | yes |  |
| `country.isoCode` | string | no | Default: `US`. |
| `text` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": "string",
      "creationTime": "string",
      "direction": "string",
      "from": {},
      "id": "string",
      "subject": "string",
      "to": [
        {}
      ],
      "type": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | string |  |
| `creationTime` | string |  |
| `direction` | string |  |
| `from` | object |  |
| `id` | string |  |
| `subject` | string |  |
| `to` | array<object> |  |
| `type` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native RingCentral API, this operation is `POST restapi/v1.0/account/:accountId/extension/:extensionId/sms` (base URL `https://platform.ringcentral.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

