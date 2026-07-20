# Action1: Check Endpoint Status

Retrieves endpoint addition status from Action1 for an organization.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/check-endpoint-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/check-endpoint-status?connectionId=$CONNECTION_ID&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/check-endpoint-status?${params}`, {
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
| `orgId` | string | yes | Provide an organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endpointsAdded": "string",
      "id": "string",
      "self": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpointsAdded` | string |  |
| `id` | string |  |
| `self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /endpoints/status/:orgId` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-endpoint-status.md) for the provider-specific parameters and requirements.

