# Instantly: Get Current Workspace

Retrieves the current workspace from Instantly.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-current-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-current-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-current-workspace?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "planId": "string",
      "planIdLeadfinder": "string",
      "timestampCreated": "string",
      "timestampUpdated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `owner` | string |  |
| `planId` | string |  |
| `planIdLeadfinder` | string |  |
| `timestampCreated` | string |  |
| `timestampUpdated` | string |  |

## Native endpoint

Through the native Instantly API, this operation is `GET /api/v2/workspaces/current` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-workspace.md) for the provider-specific parameters and requirements.

