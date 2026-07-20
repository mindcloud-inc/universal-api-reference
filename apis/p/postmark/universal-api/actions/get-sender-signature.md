# Postmark: Get Sender Signature

Retrieves a sender signature from Postmark.

```
GET https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-sender-signature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-sender-signature?connectionId=$CONNECTION_ID&signatureId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-sender-signature?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

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

Through the native Postmark API, this operation is `GET /senders/:signatureId` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sender-signature.md) for the provider-specific parameters and requirements.

