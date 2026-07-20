# xMatters: Create a plan form

Creates a plan form in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-plan-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-plan-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-plan-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no |  |
| `name` | string | no |  |
| `planId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiEnabled": true,
      "description": "string",
      "formId": "string",
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "mobileEnabled": true,
      "name": "Ava Chen",
      "plan": {
        "id": "string",
        "name": "Ava Chen",
        "planType": "string"
      },
      "recipients": {
        "count": 1,
        "links": {
          "self": "https://example.com"
        },
        "total": 1
      },
      "responseOptions": {
        "count": 1,
        "links": {
          "self": "https://example.com"
        },
        "total": 1
      },
      "scenarios": {
        "count": 1,
        "links": {
          "self": "https://example.com"
        },
        "total": 1
      },
      "triggerType": "string",
      "uiEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiEnabled` | boolean |  |
| `description` | string |  |
| `formId` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `mobileEnabled` | boolean |  |
| `name` | string |  |
| `plan.id` | string |  |
| `plan.name` | string |  |
| `plan.planType` | string |  |
| `recipients.count` | number |  |
| `recipients.links.self` | string |  |
| `recipients.total` | number |  |
| `responseOptions.count` | number |  |
| `responseOptions.links.self` | string |  |
| `responseOptions.total` | number |  |
| `scenarios.count` | number |  |
| `scenarios.links.self` | string |  |
| `scenarios.total` | number |  |
| `triggerType` | string |  |
| `uiEnabled` | boolean |  |

## Native endpoint

Through the native xMatters API, this operation is `POST plans/{planId}/forms` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-plan-form.md) for the provider-specific parameters and requirements.

