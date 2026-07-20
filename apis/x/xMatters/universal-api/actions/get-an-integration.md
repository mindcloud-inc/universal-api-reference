# xMatters: Get an integration

Retrieves an integration from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-integration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-integration?${params}`, {
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
| `integrationId` | string | no |  |
| `planId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deployed": true,
      "environment": "string",
      "form": {
        "id": "string"
      },
      "id": "string",
      "integrationType": "string",
      "name": "Ava Chen",
      "operation": "string",
      "plan": {
        "id": "string"
      },
      "script": "string",
      "triggeredBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deployed` | boolean |  |
| `environment` | string |  |
| `form.id` | string |  |
| `id` | string |  |
| `integrationType` | string |  |
| `name` | string |  |
| `operation` | string |  |
| `plan.id` | string |  |
| `script` | string |  |
| `triggeredBy` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `GET plans/{planId}/integrations/{integrationId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-integration.md) for the provider-specific parameters and requirements.

