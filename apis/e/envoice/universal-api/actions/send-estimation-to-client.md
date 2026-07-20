# Envoice: Send Estimation to Client

Sends an estimation to a client in Envoice.

```
PUT https://connect.mindcloud.co/v1/universal/envoice/latest/actions/send-estimation-to-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/send-estimation-to-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "estimationId": 1,
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/send-estimation-to-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "estimationId": 1,
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachPdf` | boolean | no | Whether to attach a PDF to the email. |
| `estimationId` | number | yes | Estimation identifier to send. |
| `message` | string | yes | Message to include in the estimation email. |
| `sendToSelf` | boolean | no | Whether to send a copy to the account owner. |
| `subject` | string | no | Email subject. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | number | Sent estimation identifier. |

## Native endpoint

Through the native Envoice API, this operation is `POST estimation/sendtoclient` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-estimation-to-client.md) for the provider-specific parameters and requirements.

