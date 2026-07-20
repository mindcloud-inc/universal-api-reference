# Postmark: Update Sender Signature

Updates a sender signature in Postmark.

```
PUT https://connect.mindcloud.co/v1/universal/postmark/latest/actions/update-sender-signature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/update-sender-signature" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmark/latest/actions/update-sender-signature', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureId` | string | yes | The Postmark sender signature ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Confirmed": true,
      "DKIMVerified": true,
      "Domain": "string",
      "EmailAddress": "ava@example.com",
      "ID": 1,
      "Name": "Ava Chen",
      "ReplyToEmailAddress": "ava@example.com",
      "ReturnPathDomain": "string",
      "SPFVerified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Confirmed` | boolean |  |
| `DKIMVerified` | boolean |  |
| `Domain` | string |  |
| `EmailAddress` | string |  |
| `ID` | number |  |
| `Name` | string |  |
| `ReplyToEmailAddress` | string |  |
| `ReturnPathDomain` | string |  |
| `SPFVerified` | boolean |  |

## Native endpoint

Through the native Postmark API, this operation is `PUT /senders/:signatureId` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sender-signature.md) for the provider-specific parameters and requirements.

