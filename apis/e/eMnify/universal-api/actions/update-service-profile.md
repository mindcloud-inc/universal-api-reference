# EMnify: Update Service Profile

Updates an existing service profile in EMnify.

```
PUT https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/update-service-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/update-service-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authToken": "string",
  "profileId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/update-service-profile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authToken": "string",
    "profileId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. |
| `profileId` | number | yes | Service profile ID. |
| `name` | string | no | Updated service profile name. |
| `description` | string | no | Updated service profile description. |
| `allowed4g` | boolean | no | Allow 4G/LTE and LTE-M connectivity. |
| `applyDataQuota` | boolean | no | Apply data quota limits. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `breakoutRegion.id` | number | no | Breakout region ID. |
| `dns.id` | number | no | DNS configuration ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applyDataQuota": true,
      "description": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applyDataQuota` | boolean |  |
| `description` | string |  |
| `id` | number |  |

## Native endpoint

Through the native EMnify API, this operation is `PATCH /service_profile/:profile_id` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service-profile.md) for the provider-specific parameters and requirements.

