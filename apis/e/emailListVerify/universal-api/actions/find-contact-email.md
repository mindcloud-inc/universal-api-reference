# EmailListVerify: Find Contact Email

Finds a contact email in EmailListVerify by name or domain.

```
GET https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/find-contact-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailListVerify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/find-contact-email?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/find-contact-email?${params}`, {
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
| `domain` | string | yes | Company email domain to search, such as example.com. |
| `firstName` | string | no | Optional contact first name. |
| `lastName` | string | no | Optional contact last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidence": "string",
      "email": "ava@example.com",
      "internalResult": "string",
      "mxServer": "https://example.com",
      "mxServerIp": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidence` | string | Confidence level. |
| `email` | string | Possible contact email. |
| `internalResult` | string | Internal processing status. |
| `mxServer` | string | MX server hostname. |
| `mxServerIp` | string | MX server IP address. |
| `result` | string | Deliverability status. |

## Native endpoint

Through the native EmailListVerify API, this operation is `POST /api/findContact` (base URL `https://api.emaillistverify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-contact-email.md) for the provider-specific parameters and requirements.

