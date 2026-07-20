# Atera: Find agents for customer

Finds agents in Atera for a specific customer.

```
GET https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-agents-for-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-agents-for-customer?connectionId=$CONNECTION_ID&limit=25&offset=0&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-agents-for-customer?${params}`, {
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
| `customerId` | number | yes | System customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AgentID": 1,
      "AgentName": "Ava Chen",
      "Created": "string",
      "CustomerID": 1,
      "CustomerName": "Ava Chen",
      "DeviceGuid": "string",
      "DeviceType": "string",
      "IpAddresses": [
        "string"
      ],
      "LastSeen": "string",
      "MacAddresses": [
        "string"
      ],
      "MachineID": "string",
      "MachineName": "Ava Chen",
      "Modified": "string",
      "Monitored": true,
      "Online": true,
      "OS": "string",
      "OSType": "string",
      "ProductName": "Ava Chen",
      "ReportedFromIP": "string",
      "SystemName": "Ava Chen",
      "Vendor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AgentID` | number | Atera agent ID. |
| `AgentName` | string | Agent display name. |
| `Created` | string | Creation timestamp. |
| `CustomerID` | number | Owning customer ID. |
| `CustomerName` | string | Owning customer name. |
| `DeviceGuid` | string | Global device GUID. |
| `DeviceType` | string | Atera device type. |
| `IpAddresses` | array<string> | Known IP addresses. |
| `LastSeen` | string | Most recent device heartbeat timestamp. |
| `MacAddresses` | array<string> | Known MAC addresses. |
| `MachineID` | string | Atera machine identifier. |
| `MachineName` | string | Machine name. |
| `Modified` | string | Last modification timestamp. |
| `Monitored` | boolean | Whether monitoring is enabled. |
| `Online` | boolean | Whether the device is currently online. |
| `OS` | string | Operating system name. |
| `OSType` | string | Operating system family. |
| `ProductName` | string | Device product name. |
| `ReportedFromIP` | string | Last reported IP address. |
| `SystemName` | string | System name reported by Atera. |
| `Vendor` | string | Device vendor. |

## Native endpoint

Through the native Atera API, this operation is `GET /api/v3/agents/customer/:customerId` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/find-agents-for-customer.md) for the provider-specific parameters and requirements.

