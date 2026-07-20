# ProxiedMail: Get Received Email Details



```
GET https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/get-received-email-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProxiedMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/get-received-email-details?connectionId=$CONNECTION_ID&receivedEmailId=81F8AD00-0000-0000-00003CC8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "receivedEmailId": "81F8AD00-0000-0000-00003CC8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/get-received-email-details?${params}`, {
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
| `receivedEmailId` | string | yes | Example: `81F8AD00-0000-0000-00003CC8`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProxiedMail API returns.

## Native endpoint

Through the native ProxiedMail API, this operation is `GET /received-emails/:receivedEmailId` (base URL `https://proxiedmail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-received-email-details.md) for the provider-specific parameters and requirements.

