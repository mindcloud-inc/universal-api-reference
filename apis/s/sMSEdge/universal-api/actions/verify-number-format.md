# SMSEdge: Verify Number Format

Verifies phone number format in SMSEdge.

```
GET https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/verify-number-format
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSEdge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/verify-number-format?connectionId=$CONNECTION_ID&number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/verify-number-format?${params}`, {
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
| `country_id` | string | no | ID of country. Recommended to specify this parameter if phone number is local format |
| `number` | string | yes | Phone number that should be verified |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMSEdge API returns.

## Native endpoint

Through the native SMSEdge API, this operation is `POST /verify/number-simple/` (base URL `https://api.smsedge.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-number-format.md) for the provider-specific parameters and requirements.

