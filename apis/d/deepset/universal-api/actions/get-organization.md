# Deepset: Get Organization

Retrieves your current Deepset organization details.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-organization?${params}`, {
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
      "gpu_enabled": true,
      "local_builder_enabled": true,
      "max_workspaces": 1,
      "name": "Ava Chen",
      "organization_id": "string",
      "organization_type": "string",
      "pricing_plan": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gpu_enabled` | boolean |  |
| `local_builder_enabled` | boolean |  |
| `max_workspaces` | number |  |
| `name` | string |  |
| `organization_id` | string |  |
| `organization_type` | string |  |
| `pricing_plan` | string |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v1/organization` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

