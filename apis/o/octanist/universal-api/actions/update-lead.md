# Octanist: Update Lead

Updates an existing lead in Octanist.

```
PUT https://connect.mindcloud.co/v1/universal/octanist/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octanist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/octanist/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/octanist/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Lead ID to update. Highest-priority match key. Example: `lead_abc123`. |
| `email` | string | no | Lead email. Used as the second-priority match key when id is not provided. Example: `john@example.com`. |
| `phone` | string | no | Lead phone. Used as the third-priority match key when id and email are not provided. Example: `+15551234567`. |
| `status` | string | no | New lead status. Example: `won`. |
| `value` | number | no | Lead value. |
| `note` | string | no | Note to attach to the lead. |
| `lossReason` | string | no | Reason for loss when status is lost. Example: `Pricing mismatch`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Octanist API returns.

## Native endpoint

Through the native Octanist API, this operation is `PATCH /leads` (base URL `https://octanist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

