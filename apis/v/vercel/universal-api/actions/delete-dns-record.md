# Vercel: Delete DNS Record

Deletes an existing DNS record from Vercel.

```
DELETE https://connect.mindcloud.co/v1/universal/vercel/latest/actions/delete-dns-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/delete-dns-record?connectionId=$CONNECTION_ID&domain=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/delete-dns-record?${params}`, {
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
| `domain` | string | yes | The domain name that owns the DNS record. |
| `recordId` | string | yes | The DNS record ID to remove. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vercel API returns.

## Native endpoint

Through the native Vercel API, this operation is `DELETE /v2/domains/:domain/records/:recordId` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-dns-record.md) for the provider-specific parameters and requirements.

