# Next Cloud OCS: Set User Preferences

Sets user preferences in Next Cloud OCS.

```
PUT https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/set-user-preferences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/set-user-preferences" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "config": {},
  "preferenceAppId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/set-user-preferences', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "config": {},
    "preferenceAppId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `config` | object | yes | Key-value preference object. |
| `preferenceAppId` | string | yes | Nextcloud preference namespace app ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": "string",
      "statuscode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | string |  |
| `statuscode` | number |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `POST /ocs/v2.php/apps/provisioning_api/api/v1/config/users/{{preferenceAppId}}` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-user-preferences.md) for the provider-specific parameters and requirements.

