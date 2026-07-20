# Memix: Get Referrals Status

Retrieves current referral status from Memix.

```
GET https://connect.mindcloud.co/v1/universal/memix/latest/actions/get-referrals-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memix/latest/actions/get-referrals-status?connectionId=$CONNECTION_ID&installation_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "installation_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memix/latest/actions/get-referrals-status?${params}`, {
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
| `installation_id` | string | yes | Installation identifier that Memix expects in the x-installation-id header. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Memix API returns.

## Native endpoint

Through the native Memix API, this operation is `GET /v1/referrals-status` (base URL `https://api.memix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-referrals-status.md) for the provider-specific parameters and requirements.

