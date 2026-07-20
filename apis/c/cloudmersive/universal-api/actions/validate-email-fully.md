# Cloudmersive: Validate Email Fully

Fully validates an email address in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-email-fully
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-email-fully?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-email-fully?${params}`, {
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
| `email` | string | no | Email address to validate fully. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "isCatchallDomain": true,
      "isDisposable": true,
      "isFreeEmailProvider": true,
      "mailServerUsedForValidation": "string",
      "validAddress": true,
      "validDomain": true,
      "validSmtp": true,
      "validSyntax": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `isCatchallDomain` | boolean |  |
| `isDisposable` | boolean |  |
| `isFreeEmailProvider` | boolean |  |
| `mailServerUsedForValidation` | string |  |
| `validAddress` | boolean |  |
| `validDomain` | boolean |  |
| `validSmtp` | boolean |  |
| `validSyntax` | boolean |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/email/address/full` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email-fully.md) for the provider-specific parameters and requirements.

