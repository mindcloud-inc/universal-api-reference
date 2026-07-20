# Recurly: Fetch Preview Renewal



```
GET https://connect.mindcloud.co/v1/universal/recurly/latest/actions/fetch-preview-renewal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recurly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/fetch-preview-renewal?connectionId=$CONNECTION_ID&subscriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurly/latest/actions/fetch-preview-renewal?${params}`, {
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
| `subscriptionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chargeInvoice": {},
      "creditInvoices": [
        {}
      ],
      "object": "string",
      "verificationTransactions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chargeInvoice` | object |  |
| `creditInvoices` | array<object> |  |
| `object` | string |  |
| `verificationTransactions` | array<object> |  |

## Native endpoint

Through the native Recurly API, this operation is `GET /subscriptions/:subscription_id/preview_renewal` (base URL `https://v3.recurly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-preview-renewal.md) for the provider-specific parameters and requirements.

