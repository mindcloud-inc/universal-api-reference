# Loqate: Batch Validate Emails

Validates multiple email addresses with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/batch-validate-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/batch-validate-emails?connectionId=$CONNECTION_ID&emails=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emails": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/batch-validate-emails?${params}`, {
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
| `emails` | string | yes | Comma-separated email addresses to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "domain": "string",
      "emailAddress": "ava@example.com",
      "isDisposible": true,
      "isSystemMailbox": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `domain` | string |  |
| `emailAddress` | string |  |
| `isDisposible` | boolean |  |
| `isSystemMailbox` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /EmailValidation/Batch/Validate/v1.20/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-validate-emails.md) for the provider-specific parameters and requirements.

