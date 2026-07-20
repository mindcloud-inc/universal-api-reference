# Vercel: Update DNS Record

Updates an existing DNS record in Vercel.

```
PUT https://connect.mindcloud.co/v1/universal/vercel/latest/actions/update-dns-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/update-dns-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vercel/latest/actions/update-dns-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recordId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The updated DNS record name. |
| `recordId` | string | yes | The DNS record ID to update. |
| `type` | string | no | The updated DNS record type. |
| `value` | string | no | The updated DNS record value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vercel API returns.

## Native endpoint

Through the native Vercel API, this operation is `PATCH /v1/domains/records/:recordId` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dns-record.md) for the provider-specific parameters and requirements.

