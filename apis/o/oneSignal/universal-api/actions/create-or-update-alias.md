# OneSignal: Create or Update Alias

Creates or updates a user alias in OneSignal.

```
PUT https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-or-update-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-or-update-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "aliasId": "string",
  "aliasLabel": "string",
  "identity": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-or-update-alias', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "aliasId": "string",
    "aliasLabel": "string",
    "identity": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aliasId` | string | yes | The alias value for the selected alias label. |
| `aliasLabel` | string | yes | The alias namespace to look up, such as external_id. |
| `identity` | object | yes | An object of aliases to create or update on the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "identity": {
        "externalId": "string",
        "onesignalId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identity.externalId` | string |  |
| `identity.onesignalId` | string |  |

## Native endpoint

Through the native OneSignal API, this operation is `PATCH /apps/:app_id/users/by/:alias_label/:alias_id/identity` (base URL `https://api.onesignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-alias.md) for the provider-specific parameters and requirements.

