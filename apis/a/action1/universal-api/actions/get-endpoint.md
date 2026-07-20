# Action1: Get Endpoint

Retrieves a managed endpoint from Action1 by ID.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-endpoint?connectionId=$CONNECTION_ID&orgId=string&endpointId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "string",
  "endpointId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-endpoint?${params}`, {
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
| `endpointId` | string | yes | Provide an endpoint ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AD_organization_unit": "string",
      "AD_security_groups": "string",
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

Through the native Action1 API, this operation is `GET /endpoints/managed/:orgId/:endpointId` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-endpoint.md) for the provider-specific parameters and requirements.

