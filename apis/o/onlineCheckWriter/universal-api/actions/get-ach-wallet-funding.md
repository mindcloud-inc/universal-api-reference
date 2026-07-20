# OnlineCheckWriter: Get ACH Wallet Funding

Retrieves the status and details of a specific ACH wallet funding request.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-ach-wallet-funding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-ach-wallet-funding?connectionId=$CONNECTION_ID&walletFundingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "walletFundingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-ach-wallet-funding?${params}`, {
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
| `walletFundingId` | string | yes | The wallet funding identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnlineCheckWriter API returns.

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /wallet/fund-wallet/:walletFundingId` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ach-wallet-funding.md) for the provider-specific parameters and requirements.

