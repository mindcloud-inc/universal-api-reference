# LoginRadius: Create Custom Object

Creates a new custom object in LoginRadius.

```
POST https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-custom-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-custom-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accessToken": "Access token",
  "objectName": "stage3Object",
  "objectRecordId": "record-1",
  "label": "Stage 3 Seed Record"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-custom-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accessToken": "Access token",
    "objectName": "stage3Object",
    "objectRecordId": "record-1",
    "label": "Stage 3 Seed Record"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessToken` | string | yes | Access token for the logged-in user. Example: `Access token`. |
| `objectName` | string | yes | Custom object collection name. Example: `stage3Object`. |
| `objectRecordId` | string | yes | Custom object record id. Example: `record-1`. |
| `label` | string | yes | Label stored in the custom object body. Example: `Stage 3 Seed Record`. |
| `active` | boolean | no | Whether the custom object is active. Example: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LoginRadius API returns.

## Native endpoint

Through the native LoginRadius API, this operation is `POST /identity/v2/auth/customobject` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-object.md) for the provider-specific parameters and requirements.

