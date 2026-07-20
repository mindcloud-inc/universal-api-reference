# UpGuard: List Vendor Vulnerabilities

Retrieves potential vulnerabilities for a vendor in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-vulnerabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-vulnerabilities?connectionId=$CONNECTION_ID&primaryHostname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "primaryHostname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-vulnerabilities?${params}`, {
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
| `primaryHostname` | string | yes | The primary hostname of the vendor to return vulnerabilities for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UpGuard API returns.

## Native endpoint

Through the native UpGuard API, this operation is `GET /vulnerabilities/vendor` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vendor-vulnerabilities.md) for the provider-specific parameters and requirements.

