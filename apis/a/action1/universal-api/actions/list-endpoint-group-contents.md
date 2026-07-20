# Action1: List Endpoint Group Contents

Retrieves endpoint group contents from Action1 by group ID.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-endpoint-group-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-endpoint-group-contents?connectionId=$CONNECTION_ID&limit=25&offset=0&orgId=string&groupId=group-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "orgId": "string",
  "groupId": "group-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-endpoint-group-contents?${params}`, {
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
| `orgId` | string | yes | Action1 organization ID. |
| `groupId` | string | yes | Endpoint group ID. Example: `group-123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AD_organization_unit": "string",
      "AD_security_groups": "string",
      "added_via": "string",
      "address": "string",
      "agent_install_date": "string",
      "agent_version": "string",
      "architecture": "string",
      "comment": "string",
      "CPU_model": "string",
      "CPU_name": "Ava Chen",
      "CPU_size": "string",
      "custom": "string",
      "device_name": "Ava Chen",
      "disk": "string",
      "id": "string",
      "last_boot_time": "string",
      "last_seen": "string",
      "MAC": "string",
      "manufacturer": "string",
      "missing_updates": "string",
      "name": "Ava Chen",
      "NIC": "string",
      "online_status": "string",
      "organization_id": "string",
      "OS": "string",
      "platform": "string",
      "RAM": "string",
      "reboot_required": "string",
      "self": "string",
      "serial": "string",
      "status": "string",
      "subscription_status": "string",
      "type": "string",
      "update_status": "string",
      "user": "string",
      "video": "string",
      "vulnerabilities": "string",
      "vulnerability_status": "string",
      "WiFi": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AD_organization_unit` | string |  |
| `AD_security_groups` | string |  |
| `added_via` | string |  |
| `address` | string |  |
| `agent_install_date` | string |  |
| `agent_version` | string |  |
| `architecture` | string |  |
| `comment` | string |  |
| `CPU_model` | string |  |
| `CPU_name` | string |  |
| `CPU_size` | string |  |
| `custom` | string |  |
| `device_name` | string |  |
| `disk` | string |  |
| `id` | string |  |
| `last_boot_time` | string |  |
| `last_seen` | string |  |
| `MAC` | string |  |
| `manufacturer` | string |  |
| `missing_updates` | string |  |
| `name` | string |  |
| `NIC` | string |  |
| `online_status` | string |  |
| `organization_id` | string |  |
| `OS` | string |  |
| `platform` | string |  |
| `RAM` | string |  |
| `reboot_required` | string |  |
| `self` | string |  |
| `serial` | string |  |
| `status` | string |  |
| `subscription_status` | string |  |
| `type` | string |  |
| `update_status` | string |  |
| `user` | string |  |
| `video` | string |  |
| `vulnerabilities` | string |  |
| `vulnerability_status` | string |  |
| `WiFi` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /endpoints/groups/:orgId/:groupId/contents` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-endpoint-group-contents.md) for the provider-specific parameters and requirements.

