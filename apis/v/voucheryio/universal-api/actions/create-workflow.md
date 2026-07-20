# Vouchery.io: Create Workflow



```
POST https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "firstActionId": "string",
  "name": "Ava Chen",
  "actions[]": [
    {}
  ],
  "metadata": {},
  "expiresIn": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "firstActionId": "string",
    "name": "Ava Chen",
    "actions[]": [{}],
    "metadata": {},
    "expiresIn": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Workflow type. Reactive or birthday. |
| `firstActionId` | string | yes | ID of the first workflow action. |
| `name` | string | yes | Workflow name. |
| `actions[]` | array<object> | yes | Workflow action graph. |
| `metadata` | object | yes | Workflow metadata object. |
| `expiresIn` | string | yes | Workflow expiry duration string. |
| `namespace` | string | no | Workflow namespace. |
| `beforeBirthday` | number | no | Days before birthday for birthday workflows. |
| `launchCriteria` | object | no | Launch criteria filter definition. |
| `validFrom` | string | no | Workflow validity start. |
| `validTo` | string | no | Workflow validity end. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchery.io API returns.

## Native endpoint

Through the native Vouchery.io API, this operation is `POST /workflows` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow.md) for the provider-specific parameters and requirements.

