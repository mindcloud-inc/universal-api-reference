# Pinghome: Create Ruleset

Creates a new ruleset in Pinghome.

```
POST https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-ruleset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-ruleset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ruleType": "state-change",
  "conditions": "string",
  "level": "team",
  "teamId": "2a85fda9-2f9b-4daf-b040-f30a835cafa5",
  "name": "CPU Spike Rule",
  "description": "Create an incident when CPU count equals threshold",
  "urgency": "medium"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-ruleset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ruleType": "state-change",
    "conditions": "string",
    "level": "team",
    "teamId": "2a85fda9-2f9b-4daf-b040-f30a835cafa5",
    "name": "CPU Spike Rule",
    "description": "Create an incident when CPU count equals threshold",
    "urgency": "medium"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ruleType` | string | yes | Type of rule to create. Example: `state-change`. |
| `conditions` | string<object> | yes | JSON array of ruleset conditions. |
| `level` | string | yes | Level for the rule. Example: `team`. |
| `teamId` | string | yes | Target team ID for the ruleset. Example: `2a85fda9-2f9b-4daf-b040-f30a835cafa5`. |
| `name` | string | yes | Ruleset name. Example: `CPU Spike Rule`. |
| `description` | string | yes | Ruleset description. Example: `Create an incident when CPU count equals threshold`. |
| `urgency` | string | yes | Urgency level for generated incidents. Example: `medium`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignees` | string<object> | no | Optional JSON array of assignee objects. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `POST https://incident-cmd.api.pinghome.io/v1/ruleset` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ruleset.md) for the provider-specific parameters and requirements.

