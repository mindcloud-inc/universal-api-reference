# EMnify: List Service Profiles

Retrieves a list of service profiles from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-service-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-service-profiles?connectionId=$CONNECTION_ID&authToken=Paste%20the%20auth_token%20from%20Retrieve%20Authentication%20Token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "Paste the auth_token from Retrieve Authentication Token"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-service-profiles?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowed2g": "string",
      "allowed3g": "string",
      "allowed4g": "string",
      "allowedNbIot": "string",
      "allowedNbIotGeo": "string",
      "apiCallback": {},
      "apiSecret": {},
      "applyDataQuota": "string",
      "applyQuota": "string",
      "applySmsQuota": "string",
      "breakoutRegion": {
        "id": 1,
        "ipAddress": "string",
        "name": "Ava Chen"
      },
      "description": "string",
      "dns": {},
      "esmeInterfaceType": {},
      "id": 1,
      "mocCallbackId": {},
      "name": "Ava Chen",
      "nipdp": "string",
      "organisationId": "string",
      "prepaid": "string",
      "retail": "string",
      "smsP2pExt": "string",
      "smsP2pInt": "string",
      "usedCount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowed2g` | string |  |
| `allowed3g` | string |  |
| `allowed4g` | string |  |
| `allowedNbIot` | string |  |
| `allowedNbIotGeo` | string |  |
| `apiCallback` | object |  |
| `apiSecret` | object |  |
| `applyDataQuota` | string |  |
| `applyQuota` | string |  |
| `applySmsQuota` | string |  |
| `breakoutRegion.id` | number |  |
| `breakoutRegion.ipAddress` | string |  |
| `breakoutRegion.name` | string |  |
| `description` | string |  |
| `dns` | object |  |
| `esmeInterfaceType` | object |  |
| `id` | number |  |
| `mocCallbackId` | object |  |
| `name` | string |  |
| `nipdp` | string |  |
| `organisationId` | string |  |
| `prepaid` | string |  |
| `retail` | string |  |
| `smsP2pExt` | string |  |
| `smsP2pInt` | string |  |
| `usedCount` | string |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /service_profile` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-profiles.md) for the provider-specific parameters and requirements.

