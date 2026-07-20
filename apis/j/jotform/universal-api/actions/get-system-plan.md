# Jotform: Get System Plan

Retrieves a system plan from Jotform.

```
GET https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-system-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-system-plan?connectionId=$CONNECTION_ID&planName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-system-plan?${params}`, {
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
| `planName` | string | yes | Plan name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "isVisible": true,
      "limits": {},
      "name": "Ava Chen",
      "prices": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `isVisible` | boolean |  |
| `limits` | object |  |
| `name` | string |  |
| `prices` | object |  |

## Native endpoint

Through the native Jotform API, this operation is `GET /system/plan/:planName` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-system-plan.md) for the provider-specific parameters and requirements.

