# Zoho Connect: Get All Network Members

Retrieves all network members from Zoho Connect.

```
GET https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-network-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-network-members?connectionId=$CONNECTION_ID&scopeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scopeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-network-members?${params}`, {
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
| `scopeId` | string | yes | Network ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canFollow": "string",
      "emailId": "ava@example.com",
      "id": "string",
      "imageUrl": "https://example.com",
      "isFollowing": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "role": "string",
      "status": "string",
      "type": "string",
      "workLocation": "string",
      "zuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canFollow` | string |  |
| `emailId` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `isFollowing` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `role` | string |  |
| `status` | string |  |
| `type` | string |  |
| `workLocation` | string |  |
| `zuid` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `GET /pulse/api/orgMembers` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-network-members.md) for the provider-specific parameters and requirements.

