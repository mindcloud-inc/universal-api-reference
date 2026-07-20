# Unleash: Get Application Environment Instances (Last 24H)

Retrieves application environment instances (Last 24h) from Unleash.

```
GET https://connect.mindcloud.co/v1/universal/unleash/latest/actions/getapplicationenvironmentinstances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleash/latest/actions/getapplicationenvironmentinstances?connectionId=$CONNECTION_ID&appName=Ava%20Chen&environment=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appName": "Ava Chen",
  "environment": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleash/latest/actions/getapplicationenvironmentinstances?${params}`, {
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
| `appName` | string | yes | Required path parameter. |
| `environment` | string | yes | Required path parameter. |

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

Through the native Unleash API, this operation is `GET /api/admin/metrics/instances/{appName}/environment/{environment}` (base URL `https://us.app.getunleash.io/uspp0456`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/getapplicationenvironmentinstances.md) for the provider-specific parameters and requirements.

