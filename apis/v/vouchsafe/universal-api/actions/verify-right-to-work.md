# Vouchsafe: Verify Right To Work

Verifies right to work with a UK eVisa in Vouchsafe.

```
POST https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/verify-right-to-work
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchsafe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/verify-right-to-work" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload.companyName": "Ava Chen",
  "payload.dateOfBirth": "string",
  "payload.shareCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/verify-right-to-work', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload.companyName": "Ava Chen",
    "payload.dateOfBirth": "string",
    "payload.shareCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | object | no | The right to work verification payload. |
| `payload.companyName` | string | yes | Name of the company requesting the verification. |
| `payload.dateOfBirth` | string | yes | Date of birth in YYYY-MM-DD or ISO 8601 format. |
| `payload.shareCode` | string | yes | The 9-character share code from the UK Home Office. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchsafe API returns.

## Native endpoint

Through the native Vouchsafe API, this operation is `POST /verify/evisa` (base URL `https://app.vouchsafe.id/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-right-to-work.md) for the provider-specific parameters and requirements.

