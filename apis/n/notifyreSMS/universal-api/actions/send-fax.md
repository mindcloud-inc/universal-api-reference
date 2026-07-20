# Notifyre SMS: Send Fax

Creates a fax message in Notifyre.

```
POST https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/send-fax
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/send-fax" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documents": {},
  "recipients": {},
  "sendFrom": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/send-fax', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documents": {},
    "recipients": {},
    "sendFrom": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documents` | list<object> | yes | Documents to upload and send as fax pages. |
| `recipients` | list<object> | yes | Fax recipients. |
| `sendFrom` | string | yes | Fax number or sender identifier used to send. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchID": "string",
      "friendlyID": "string",
      "invalidToNumbers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchID` | string | Identifier of the submitted fax batch. |
| `friendlyID` | string | Human-friendly fax batch reference. |
| `invalidToNumbers` | array<object> | Rejected fax recipients, if any. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `POST /fax/send` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-fax.md) for the provider-specific parameters and requirements.

