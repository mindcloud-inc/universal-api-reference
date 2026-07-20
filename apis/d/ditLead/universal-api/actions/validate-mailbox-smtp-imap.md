# DitLead: Validate Mailbox SMTP IMAP



```
GET https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/validate-mailbox-smtp-imap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/validate-mailbox-smtp-imap?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/validate-mailbox-smtp-imap?${params}`, {
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
| `imap.host` | string | no |  |
| `imap.password` | string | no |  |
| `imap.port` | string | no |  |
| `imap.username` | string | no |  |
| `smtp.emailAddress` | string | no |  |
| `smtp.host` | string | no |  |
| `smtp.password` | string | no |  |
| `smtp.port` | string | no |  |
| `smtp.secure` | boolean | no |  |
| `smtp.username` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": [
        "string"
      ],
      "eventId": [
        "string"
      ],
      "success": true,
      "updatedAt": [
        "string"
      ],
      "url": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | array<string> |  |
| `eventId` | array<string> |  |
| `success` | boolean |  |
| `updatedAt` | array<string> |  |
| `url` | array<string> |  |

## Native endpoint

Through the native DitLead API, this operation is `POST /v1/mailbox/validate` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-mailbox-smtp-imap.md) for the provider-specific parameters and requirements.

