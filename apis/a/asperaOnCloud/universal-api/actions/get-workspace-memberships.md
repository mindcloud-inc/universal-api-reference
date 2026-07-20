# Aspera on Cloud: List Workspace Members

Retrieves workspace members from Aspera on Cloud.

```
GET https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-workspace-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspera on Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-workspace-memberships?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-workspace-memberships?${params}`, {
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
      "inherited": true,
      "manager": true,
      "member_id": 1,
      "member_type": "string",
      "running_operation_count": 1,
      "stopped_operation_count": 1,
      "storage_allowed": true,
      "workspace_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `inherited` | boolean |  |
| `manager` | boolean |  |
| `member_id` | number |  |
| `member_type` | string |  |
| `running_operation_count` | number |  |
| `stopped_operation_count` | number |  |
| `storage_allowed` | boolean |  |
| `workspace_id` | number |  |

## Native endpoint

Through the native Aspera on Cloud API, this operation is `GET /v1/workspace_memberships` (base URL `https://api.ibmaspera.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-memberships.md) for the provider-specific parameters and requirements.

