# v0: Get Billing

Retrieves billing details for the current user in v0.

```
GET https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-billing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-billing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-billing?${params}`, {
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
| `scope` | string | no | Optionally scope billing data to a project ID or slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingType": "string",
      "data": {
        "balance": {
          "remaining": 1,
          "total": 1
        },
        "billingCycle": {
          "end": 1,
          "start": 1
        },
        "onDemand": {
          "balance": 1
        },
        "plan": "string",
        "role": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingType` | string |  |
| `data.balance.remaining` | number |  |
| `data.balance.total` | number |  |
| `data.billingCycle.end` | number |  |
| `data.billingCycle.start` | number |  |
| `data.onDemand.balance` | number |  |
| `data.plan` | string |  |
| `data.role` | string |  |

## Native endpoint

Through the native v0 API, this operation is `GET /v1/user/billing` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billing.md) for the provider-specific parameters and requirements.

