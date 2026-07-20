# Unleash: Adds A Strategy To A Milestone.

Adds a strategy to a milestone in Unleash.

```
POST https://connect.mindcloud.co/v1/universal/unleash/latest/actions/post-api-admin-release-plan-templates-templateid-milestones-milestoneid-strategies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unleash/latest/actions/post-api-admin-release-plan-templates-templateid-milestones-milestoneid-strategies" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "milestoneId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unleash/latest/actions/post-api-admin-release-plan-templates-templateid-milestones-milestoneid-strategies', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "milestoneId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Required path parameter. |
| `milestoneId` | string | yes | Required path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "success": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Resource description. |
| `id` | string | Resource identifier. |
| `message` | string | Response message. |
| `name` | string | Resource name. |
| `success` | boolean | Whether the operation succeeded. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Unleash API, this operation is `POST /api/admin/release-plan-templates/{templateId}/milestones/{milestoneId}/strategies` (base URL `https://us.app.getunleash.io/uspp0456`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-api-admin-release-plan-templates-templateid-milestones-milestoneid-strategies.md) for the provider-specific parameters and requirements.

