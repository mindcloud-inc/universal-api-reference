# Clearout: Verify Email Instantly

Retrieves instant email verification results from Clearout.

```
GET https://connect.mindcloud.co/v1/universal/clearout/latest/actions/verify-email-instantly
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clearout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/verify-email-instantly?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearout/latest/actions/verify-email-instantly?${params}`, {
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
| `email` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeout` | number | no | Request wait time (in milliseconds), Maximum allowed wait time should not exceed 180,000 milliseconds Default: `130000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounceType": "string",
      "detailInfo": {
        "account": "string",
        "domain": "string"
      },
      "disposable": "string",
      "emailAddress": "ava@example.com",
      "free": "string",
      "gibberish": "string",
      "profile": "string",
      "role": "string",
      "safeToSend": "string",
      "status": "string",
      "subStatus": {
        "code": 1,
        "desc": "string"
      },
      "suggestedEmailAddress": "ava@example.com",
      "timeTaken": 1,
      "verifiedOn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounceType` | string |  |
| `detailInfo` | object |  |
| `detailInfo.account` | string |  |
| `detailInfo.domain` | string |  |
| `disposable` | string |  |
| `emailAddress` | string |  |
| `free` | string |  |
| `gibberish` | string |  |
| `profile` | string |  |
| `role` | string |  |
| `safeToSend` | string |  |
| `status` | string |  |
| `subStatus` | object |  |
| `subStatus.code` | number |  |
| `subStatus.desc` | string |  |
| `suggestedEmailAddress` | string |  |
| `timeTaken` | number |  |
| `verifiedOn` | string |  |

## Native endpoint

Through the native Clearout API, this operation is `POST /email_verify/instant` (base URL `https://api.clearout.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-instantly.md) for the provider-specific parameters and requirements.

