# Routee: Check Verification Status

Retrieves the verification status from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-verification-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-verification-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-verification-status?${params}`, {
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
| `requestId` | string | yes | Unique identifier from the checkSendAbility method |
| `code` | string | no | The code entered by the user. If provided, the method checks if the code is valid for the relevant request |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `POST /telegram/checkVerificationStatus` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-verification-status.md) for the provider-specific parameters and requirements.

