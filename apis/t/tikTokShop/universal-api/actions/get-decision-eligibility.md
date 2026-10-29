# TikTok Shop: Get Decision Eligibility



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-decision-eligibility
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-decision-eligibility?connectionId=$CONNECTION_ID&returnOrCancelId=string&shopCipher=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "returnOrCancelId": "string",
  "shopCipher": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-decision-eligibility?${params}`, {
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
| `returnOrCancelId` | string | yes | Use a return or cancellation request ID, rather than an order ID. |
| `shopCipher` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkDecisions` | list<string> | no | One of: `APPROVE_RECEIVED_PACKAGE`, `APPROVE_REFUND`, `APPROVE_REPLACEMENT`, `APPROVE_REQUEST_CANCEL`, `APPROVE_RETURN`, `DIRECT_REFUND`, `ISSUE_EXCHANGE_REFUND`, `ISSUE_REPLACEMENT_REFUND`, `REJECT_RECEIVED_PACKAGE`, `REJECT_REFUND`, `REJECT_REPLACEMENT`, `REJECT_REQUEST_CANCEL`, `REJECT_RETURN`. Accepts multiple values in one string, delimited by `,`. |
| `locale` | string | no | Default: `en-US`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `GET /return_refund/202601/decision_eligibility` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-decision-eligibility.md) for the provider-specific parameters and requirements.

