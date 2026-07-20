# Postmark: Create Sender Signature

Creates a sender signature in Postmark.

```
POST https://connect.mindcloud.co/v1/universal/postmark/latest/actions/create-sender-signature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/create-sender-signature" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmark/latest/actions/create-sender-signature', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native Postmark API, this operation is `POST /senders` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sender-signature.md) for the provider-specific parameters and requirements.

