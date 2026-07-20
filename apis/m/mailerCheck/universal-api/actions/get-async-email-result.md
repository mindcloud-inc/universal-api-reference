# MailerCheck: Get Async Email Result

Retrieves an asynchronous email verification result from MailerCheck.

```
GET https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-async-email-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-async-email-result?connectionId=$CONNECTION_ID&verificationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "verificationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-async-email-result?${params}`, {
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
| `verificationId` | string | yes | Async verification identifier returned by Verify Single Email Async. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "result": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `result` | string |  |
| `state` | string |  |

## Native endpoint

Through the native MailerCheck API, this operation is `GET /check/single-async/:verification_id` (base URL `https://app.mailercheck.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-email-result.md) for the provider-specific parameters and requirements.

