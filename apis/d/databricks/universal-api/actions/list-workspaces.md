# Databricks: List Workspaces

Retrieves workspaces from the Databricks account.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-workspaces?${params}`, {
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
      "account_id": "string",
      "aws_region": "string",
      "compute_mode": "string",
      "creation_time": 1,
      "deployment_name": "Ava Chen",
      "identity_federation_info": {},
      "is_no_public_ip_enabled": true,
      "pricing_tier": "string",
      "workspace_fqdn": "string",
      "workspace_id": 1,
      "workspace_info": {},
      "workspace_name": "Ava Chen",
      "workspace_status": "string",
      "workspace_status_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `aws_region` | string |  |
| `compute_mode` | string |  |
| `creation_time` | number |  |
| `deployment_name` | string |  |
| `identity_federation_info` | object |  |
| `is_no_public_ip_enabled` | boolean |  |
| `pricing_tier` | string |  |
| `workspace_fqdn` | string |  |
| `workspace_id` | number |  |
| `workspace_info` | object |  |
| `workspace_name` | string |  |
| `workspace_status` | string |  |
| `workspace_status_message` | string |  |

## Native endpoint

Through the native Databricks API, this operation is `GET /api/2.0/accounts/{{credentials.accountId}}/workspaces` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

