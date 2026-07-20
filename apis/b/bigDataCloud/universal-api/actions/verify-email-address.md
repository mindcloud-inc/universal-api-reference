# BigDataCloud: Verify Email Address

Verifies an email address in BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/verify-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/verify-email-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/verify-email-address?${params}`, {
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
| `emailAddress` | string | no | Email address to verify. Example: `support@bigdatacloud.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inputData": "string",
      "isDisposable": true,
      "isKnownSpammerDomain": true,
      "isMailServerDefined": true,
      "isSyntaxValid": true,
      "isValid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inputData` | string |  |
| `isDisposable` | boolean |  |
| `isKnownSpammerDomain` | boolean |  |
| `isMailServerDefined` | boolean |  |
| `isSyntaxValid` | boolean |  |
| `isValid` | boolean |  |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/email-verify` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-address.md) for the provider-specific parameters and requirements.

