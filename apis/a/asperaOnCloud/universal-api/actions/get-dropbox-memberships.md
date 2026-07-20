# Aspera on Cloud: List Dropbox Members

Retrieves shared inbox members from Aspera on Cloud.

```
GET https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-dropbox-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspera on Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-dropbox-memberships?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-dropbox-memberships?${params}`, {
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
      "can_receive_packages": true,
      "can_submit_packages": true,
      "creator_id": "string",
      "dropbox_id": "string",
      "id": "string",
      "manager": true,
      "member_id": "string",
      "member_type": "string",
      "submit_expired": true,
      "submit_expires_at": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can_receive_packages` | boolean |  |
| `can_submit_packages` | boolean |  |
| `creator_id` | string |  |
| `dropbox_id` | string |  |
| `id` | string |  |
| `manager` | boolean |  |
| `member_id` | string |  |
| `member_type` | string |  |
| `submit_expired` | boolean |  |
| `submit_expires_at` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native Aspera on Cloud API, this operation is `GET /v1/dropbox_memberships` (base URL `https://api.ibmaspera.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dropbox-memberships.md) for the provider-specific parameters and requirements.

