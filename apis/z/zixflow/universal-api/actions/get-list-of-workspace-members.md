# Zixflow: Get List of Workspace Members

Retrieves workspace members from Zixflow.

```
GET https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-workspace-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-workspace-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-workspace-members?${params}`, {
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
      "data": [
        "string"
      ],
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array | Workspace member rows returned by Zixflow. |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the workspace-members request succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `GET /workspace-members` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-of-workspace-members.md) for the provider-specific parameters and requirements.

