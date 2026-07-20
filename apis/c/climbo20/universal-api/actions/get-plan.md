# Climbo 2.0: Get Plan

Retrieves a subscription plan from Climbo 2.0.

```
GET https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/get-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Climbo 2.0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/get-plan?connectionId=$CONNECTION_ID&planId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/get-plan?${params}`, {
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
| `planId` | string | yes | Plan ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "id": "string",
      "interval": "string",
      "link": "https://example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `currency` | string |  |
| `id` | string |  |
| `interval` | string |  |
| `link` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Climbo 2.0 API, this operation is `GET /plan/{plan_id}` (base URL `https://api.climbo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plan.md) for the provider-specific parameters and requirements.

