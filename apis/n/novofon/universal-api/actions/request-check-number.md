# Novofon: Request Check Number

Creates a number check request in Novofon.

```
POST https://connect.mindcloud.co/v1/universal/novofon/latest/actions/request-check-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novofon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/request-check-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "callerId": "string",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/novofon/latest/actions/request-check-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "callerId": "string",
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callerId` | string | yes | Caller ID number displayed for the validation call. Only numbers already connected in Novofon are allowed. |
| `code` | string | no | Optional numeric code to play during the validation call. |
| `to` | string | yes | Phone number or SIP destination to validate. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Novofon API returns.

## Native endpoint

Through the native Novofon API, this operation is `GET /v1/request/checknumber/` (base URL `https://api.novofon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-check-number.md) for the provider-specific parameters and requirements.

