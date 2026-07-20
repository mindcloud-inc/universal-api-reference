# Cloudmersive: Validate Email Syntax

Validates an email address syntactically in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-email-syntax
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-email-syntax?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-email-syntax?${params}`, {
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
| `value` | string | no | Email address to validate syntactically. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "isDisposable": true,
      "isFreeEmailProvider": true,
      "validAddress": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `isDisposable` | boolean |  |
| `isFreeEmailProvider` | boolean |  |
| `validAddress` | boolean |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/email/address/syntaxOnly` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email-syntax.md) for the provider-specific parameters and requirements.

