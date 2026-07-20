# Faraday: Get Current Account Billing

Retrieves current account billing details from Faraday.

```
GET https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-current-account-billing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faraday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-current-account-billing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-current-account-billing?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "invoices": [
        {}
      ],
      "payments": [
        {}
      ],
      "usages": [
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
| `invoices` | array<object> | Billing invoices. |
| `payments` | array<object> | Billing payments. |
| `usages` | array<object> | Usage line items. |

## Native endpoint

Through the native Faraday API, this operation is `GET /accounts/current/billing` (base URL `https://api.faraday.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-account-billing.md) for the provider-specific parameters and requirements.

