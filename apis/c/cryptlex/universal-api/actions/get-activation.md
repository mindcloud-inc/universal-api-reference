# Cryptlex: Get Activation

Retrieves an activation from Cryptlex.

```
GET https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/get-activation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/get-activation?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/get-activation?${params}`, {
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
| `id` | string | yes | Unique identifier for the activation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appVersion": "string",
      "container": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "hostname": "Ava Chen",
      "id": "string",
      "lastSyncedAt": "2026-05-07T12:00:00.000Z",
      "leaseExpiresAt": "2026-05-07T12:00:00.000Z",
      "licenseId": "string",
      "location": {},
      "metadata": [
        {}
      ],
      "meterAttributes": [
        {}
      ],
      "offline": true,
      "organization": {},
      "os": "string",
      "osVersion": "string",
      "productId": "string",
      "releaseChannel": "string",
      "releasePlatform": "string",
      "releaseVersion": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appVersion` | string |  |
| `container` | boolean |  |
| `createdAt` | date |  |
| `expiresAt` | date |  |
| `hostname` | string |  |
| `id` | string |  |
| `lastSyncedAt` | date |  |
| `leaseExpiresAt` | date |  |
| `licenseId` | string |  |
| `location` | object |  |
| `metadata` | array<object> |  |
| `meterAttributes` | array<object> |  |
| `offline` | boolean |  |
| `organization` | object |  |
| `os` | string |  |
| `osVersion` | string |  |
| `productId` | string |  |
| `releaseChannel` | string |  |
| `releasePlatform` | string |  |
| `releaseVersion` | string |  |
| `updatedAt` | date |  |
| `user` | object |  |

## Native endpoint

Through the native Cryptlex API, this operation is `GET /v3/activations/:id` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activation.md) for the provider-specific parameters and requirements.

