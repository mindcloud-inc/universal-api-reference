# 4HSE: Create Action

Creates a new action in 4HSE.

```
POST https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionType": "TRAINING",
  "name": "Fire Safety Refresher",
  "subtenantId": "2fdc699f-e67a-46dc-81a6-b03bb029dd07",
  "tenantId": "global"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionType": "TRAINING",
    "name": "Fire Safety Refresher",
    "subtenantId": "2fdc699f-e67a-46dc-81a6-b03bb029dd07",
    "tenantId": "global"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionType` | string | yes | Type of preventive action. One of: `0`, `1`, `2`, `3`, `4`. Example: `TRAINING`. |
| `code` | string | no | Identifier code for the action. Example: `ACT-001`. |
| `name` | string | yes | Descriptive name of the action. Example: `Fire Safety Refresher`. |
| `validityUnit` | string | no | Unit for the certificate validity period. One of: `0`, `1`, `2`. Example: `YEAR`. |
| `validity` | number | no | Number of validity units. Example: `1`. |
| `subtenantId` | string | yes | The office where this action is defined. Example: `2fdc699f-e67a-46dc-81a6-b03bb029dd07`. |
| `tenantId` | string | yes | The project this action belongs to. Example: `global`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional detailed description. Example: `Annual compliance activity for site workers.`. |
| `expireInterval` | number | no | Days before expiration to trigger EXPIRING status. Example: `30`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 4HSE API returns.

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/action/create` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-action.md) for the provider-specific parameters and requirements.

