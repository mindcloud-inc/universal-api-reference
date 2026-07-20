# EMnify: Create Endpoint

Creates a new endpoint in EMnify.

```
POST https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/create-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/create-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authToken": "Paste the auth_token from Retrieve Authentication Token",
  "serviceProfile.id": "1442702",
  "tariffProfile.id": "1659304",
  "status.id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/create-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authToken": "Paste the auth_token from Retrieve Authentication Token",
    "serviceProfile.id": "1442702",
    "tariffProfile.id": "1659304",
    "status.id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. Example: `Paste the auth_token from Retrieve Authentication Token`. |
| `serviceProfile.id` | number | yes | Service profile ID that determines network access settings. Example: `1442702`. |
| `tariffProfile.id` | number | yes | Tariff profile ID that determines pricing and data limits. Example: `1659304`. |
| `status.id` | number | yes | Initial endpoint status ID. Example: `1`. |
| `name` | string | no | Display name for the endpoint. Example: `MindCloud Stage 3 disposable endpoint`. |
| `tags` | string | no | Comma-separated endpoint tags. Example: `stage3,disposable`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imei` | string | no | IMEI with software version number. Example: `1234567890123456`. |
| `imeiLock` | boolean | no | Only allow connections from the specified IMEI. Example: `false`. |
| `sim.id` | number | no | SIM ID to assign to the endpoint. Example: `3595575`. |
| `sim.activate` | boolean | no | Activate the assigned SIM during endpoint creation. Example: `true`. |
| `ipAddress` | string | no | Private IP address to assign. Example: `100.80.0.10`. |
| `ipAddressSpace.id` | number | no | IP address space ID required when an IP address is provided. Example: `54036`. |
| `organisation.id` | number | no | Organization ID for reseller-created endpoints. Example: `32462`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "ipAddress": "string",
      "ipAddressSpace": {
        "id": 1
      },
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | number |  |
| `ipAddress` | string |  |
| `ipAddressSpace.id` | number |  |
| `lastUpdated` | date |  |
| `name` | string |  |

## Native endpoint

Through the native EMnify API, this operation is `POST /endpoint` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-endpoint.md) for the provider-specific parameters and requirements.

