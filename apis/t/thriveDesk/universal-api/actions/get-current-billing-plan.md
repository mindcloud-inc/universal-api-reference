# ThriveDesk: Get Current Billing Plan



```
GET https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-current-billing-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-current-billing-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-current-billing-plan?${params}`, {
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
      "licenses": [
        {}
      ],
      "overview": {},
      "subscriptions": [
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
| `licenses` | array<object> | Current licenses. |
| `overview` | object | Current plan overview. |
| `subscriptions` | array<object> | Current subscriptions. |

## Native endpoint

Through the native ThriveDesk API, this operation is `GET /v1/billing/plans/current` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-billing-plan.md) for the provider-specific parameters and requirements.

