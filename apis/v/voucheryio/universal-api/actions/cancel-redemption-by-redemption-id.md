# Vouchery.io: Cancel Redemption By Redemption ID



```
DELETE https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/cancel-redemption-by-redemption-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/cancel-redemption-by-redemption-id?connectionId=$CONNECTION_ID&redemptionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "redemptionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/cancel-redemption-by-redemption-id?${params}`, {
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
| `redemptionId` | number | yes | Redemption ID |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchery.io API returns.

## Native endpoint

Through the native Vouchery.io API, this operation is `DELETE /redemptions/:redemption_id` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-redemption-by-redemption-id.md) for the provider-specific parameters and requirements.

