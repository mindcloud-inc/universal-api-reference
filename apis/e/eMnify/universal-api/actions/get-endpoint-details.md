# EMnify: Get Endpoint Details

Retrieves details for an endpoint from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-endpoint-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-endpoint-details?connectionId=$CONNECTION_ID&authToken=Paste%20the%20auth_token%20from%20Retrieve%20Authentication%20Token&endpointId=18811970" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "Paste the auth_token from Retrieve Authentication Token",
  "endpointId": "18811970"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-endpoint-details?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. Example: `Paste the auth_token from Retrieve Authentication Token`. |
| `endpointId` | number | yes | Endpoint ID to retrieve. Example: `18811970`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "imei": {},
      "imeiLock": true,
      "imeiWithLuhn": {},
      "ipAddress": "string",
      "ipAddressSpace": {
        "id": 1,
        "ipAddressSpace": "string",
        "ipAddressVersion": 1
      },
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "serviceProfile": {
        "id": 1,
        "name": "Ava Chen"
      },
      "status": {
        "description": "string",
        "id": 1
      },
      "tags": {},
      "tariffProfile": {
        "id": 1,
        "name": "Ava Chen",
        "satelliteCapable": true
      }
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
| `imei` | object |  |
| `imeiLock` | boolean |  |
| `imeiWithLuhn` | object |  |
| `ipAddress` | string |  |
| `ipAddressSpace.id` | number |  |
| `ipAddressSpace.ipAddressSpace` | string |  |
| `ipAddressSpace.ipAddressVersion` | number |  |
| `lastUpdated` | date |  |
| `name` | string |  |
| `serviceProfile.id` | number |  |
| `serviceProfile.name` | string |  |
| `status.description` | string |  |
| `status.id` | number |  |
| `tags` | object |  |
| `tariffProfile.id` | number |  |
| `tariffProfile.name` | string |  |
| `tariffProfile.satelliteCapable` | boolean |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /endpoint/:endpoint_id` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-endpoint-details.md) for the provider-specific parameters and requirements.

