# Agent Mail: Get Organization

Retrieves the authenticated organization details from AgentMail.

```
GET https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-organization?${params}`, {
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
      "authentication_id": "string",
      "authentication_type": "string",
      "billing_id": "string",
      "billing_subscription_id": "string",
      "billing_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "domain_count": 1,
      "domain_limit": 1,
      "inbox_count": 1,
      "inbox_limit": 1,
      "organization_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authentication_id` | string | Authentication ID. |
| `authentication_type` | string | Authentication provider type. |
| `billing_id` | string | Billing customer ID. |
| `billing_subscription_id` | string | Billing subscription ID. |
| `billing_type` | string | Billing provider type. |
| `created_at` | date | Creation timestamp. |
| `domain_count` | number | Current number of domains. |
| `domain_limit` | number | Maximum number of domains allowed. |
| `inbox_count` | number | Current number of inboxes. |
| `inbox_limit` | number | Maximum number of inboxes allowed. |
| `organization_id` | string | ID of the organization. |
| `updated_at` | date | Last update timestamp. |

## Native endpoint

Through the native Agent Mail API, this operation is `GET /organizations` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

