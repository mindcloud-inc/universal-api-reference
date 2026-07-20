# Chargeflow: Get Integration By ID

Retrieves an existing integration from Chargeflow.

```
GET https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-integration-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-integration-by-id?connectionId=$CONNECTION_ID&integrationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "integrationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-integration-by-id?${params}`, {
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
| `integrationId` | string | yes | The Chargeflow integration ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "integration": {
        "name": "Ava Chen",
        "scope": "string",
        "token_type": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `integration.name` | string |  |
| `integration.scope` | string |  |
| `integration.token_type` | string |  |
| `integration.type` | string |  |

## Native endpoint

Through the native Chargeflow API, this operation is `GET /integrations/{integrationId}` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration-by-id.md) for the provider-specific parameters and requirements.

