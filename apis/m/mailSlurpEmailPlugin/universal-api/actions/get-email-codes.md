# MailSlurp Email Plugin: Get Email Codes

Extracts verification codes from an email in MailSlurp.

```
GET https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/get-email-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailSlurp Email Plugin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/get-email-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/get-email-codes?${params}`, {
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
| `emailId` | string | no | The MailSlurp email ID to inspect for verification codes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidates": [
        "string"
      ],
      "code": "string",
      "found": true,
      "methodUsed": "string",
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidates` | array<string> |  |
| `code` | string |  |
| `found` | boolean |  |
| `methodUsed` | string |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native MailSlurp Email Plugin API, this operation is `POST /emails/:emailId/codes` (base URL `https://api.mailslurp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-codes.md) for the provider-specific parameters and requirements.

