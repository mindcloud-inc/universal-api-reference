# EMnify: Create Service Profile

Creates a new service profile in EMnify.

```
POST https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/create-service-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/create-service-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authToken": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/create-service-profile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authToken": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. |
| `name` | string | yes | Service profile name. |
| `description` | string | no | Service profile description. |
| `allowed3g` | boolean | no | Allow 3G connectivity. |
| `allowed4g` | boolean | no | Allow 4G/LTE and LTE-M connectivity. |
| `allowedNbIot` | boolean | no | Allow NB-IoT connectivity. |
| `allowedNbIotGeo` | boolean | no | Allow NB-IoT connectivity over satellite networks. |
| `applySmsQuota` | boolean | no | Apply SMS quota limits. |
| `applyDataQuota` | boolean | no | Apply data quota limits. |
| `retail` | boolean | no | Retail mode flag. |
| `smsP2pInt` | boolean | no | Allow internal person-to-person SMS. |
| `smsP2pExt` | boolean | no | Allow external person-to-person SMS. |
| `nipdp` | boolean | no | Enable NIPDP. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prepaid` | boolean | no | Deprecated prepaid flag. |
| `breakoutRegion.id` | number | no | Breakout region ID. |
| `dns.id` | number | no | DNS configuration ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "serviceProfileId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `serviceProfileId` | string |  |

## Native endpoint

Through the native EMnify API, this operation is `POST /service_profile` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service-profile.md) for the provider-specific parameters and requirements.

