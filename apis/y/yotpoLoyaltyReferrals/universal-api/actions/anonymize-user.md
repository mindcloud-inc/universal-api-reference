# Yotpo Loyalty & Referrals: Anonymize User

Deletes and anonymizes user data in Yotpo Loyalty & Referrals.

```
DELETE https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/anonymize-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/anonymize-user?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/anonymize-user?${params}`, {
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
| `email` | string | yes | The email address of the end-user requesting deletion. |
| `allStores` | boolean | no | Delete the user's data across all stores in the organization when true. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yotpo Loyalty & Referrals API returns.

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `DELETE /api/v2/privacy/data` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/anonymize-user.md) for the provider-specific parameters and requirements.

