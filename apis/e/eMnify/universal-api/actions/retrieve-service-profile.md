# EMnify: Retrieve Service Profile

Retrieves a service profile from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-service-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-service-profile?connectionId=$CONNECTION_ID&authToken=string&profileId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "string",
  "profileId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-service-profile?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. |
| `profileId` | number | yes | Service profile ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowed2g": 1,
      "allowed3g": 1,
      "allowed4g": 1,
      "allowedNbIot": 1,
      "allowedNbIotGeo": 1,
      "apiCallback": {},
      "apiSecret": {},
      "applyDataQuota": 1,
      "applyQuota": 1,
      "applySmsQuota": 1,
      "breakoutRegion": {
        "id": 1,
        "ipAddress": "string",
        "name": "Ava Chen"
      },
      "description": {},
      "dns": {},
      "esmeInterfaceType": {
        "description": "string",
        "id": {}
      },
      "id": 1,
      "mocCallbackId": {},
      "name": "Ava Chen",
      "nipdp": "string",
      "organisationId": "string",
      "prepaid": 1,
      "retail": 1,
      "smppBind": {
        "dcs": "string",
        "filterDestAddress": "string",
        "id": 1,
        "isExternal": "string",
        "organisationId": "string",
        "port": {},
        "smppBindStatusId": "string",
        "smppBindTypeId": "string",
        "systemId": "string"
      },
      "smsP2pExt": 1,
      "smsP2pInt": 1,
      "usedCount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowed2g` | number |  |
| `allowed3g` | number |  |
| `allowed4g` | number |  |
| `allowedNbIot` | number |  |
| `allowedNbIotGeo` | number |  |
| `apiCallback` | object |  |
| `apiSecret` | object |  |
| `applyDataQuota` | number |  |
| `applyQuota` | number |  |
| `applySmsQuota` | number |  |
| `breakoutRegion.id` | number |  |
| `breakoutRegion.ipAddress` | string |  |
| `breakoutRegion.name` | string |  |
| `description` | object |  |
| `dns` | object |  |
| `esmeInterfaceType.description` | string |  |
| `esmeInterfaceType.id` | object |  |
| `id` | number |  |
| `mocCallbackId` | object |  |
| `name` | string |  |
| `nipdp` | string |  |
| `organisationId` | string |  |
| `prepaid` | number |  |
| `retail` | number |  |
| `smppBind.dcs` | string |  |
| `smppBind.filterDestAddress` | string |  |
| `smppBind.id` | number |  |
| `smppBind.isExternal` | string |  |
| `smppBind.organisationId` | string |  |
| `smppBind.port` | object |  |
| `smppBind.smppBindStatusId` | string |  |
| `smppBind.smppBindTypeId` | string |  |
| `smppBind.systemId` | string |  |
| `smsP2pExt` | number |  |
| `smsP2pInt` | number |  |
| `usedCount` | string |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /service_profile/:profile_id` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-service-profile.md) for the provider-specific parameters and requirements.

