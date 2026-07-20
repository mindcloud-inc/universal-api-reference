# Emailchef: Create Segment

Creates a new segment in Emailchef.

```
POST https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/create-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emailchef `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/create-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "instanceIn.listId": "string",
  "instanceIn.logic": "string",
  "instanceIn.conditionGroups[]": [
    {}
  ],
  "instanceIn.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/create-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "instanceIn.listId": "string",
    "instanceIn.logic": "string",
    "instanceIn.conditionGroups[]": [{}],
    "instanceIn.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instanceIn.listId` | string | yes |  |
| `instanceIn.logic` | string | yes |  |
| `instanceIn.conditionGroups[]` | array<object> | yes |  |
| `instanceIn.name` | string | yes |  |
| `instanceIn.description` | string | no |  |
| `instanceIn.conditionGroups[].logic` | string | no |  |
| `instanceIn.conditionGroups[].conditions[].fieldId` | string | no |  |
| `instanceIn.conditionGroups[].conditions[].name` | string | no |  |
| `instanceIn.conditionGroups[].conditions[].comparableId` | string | no |  |
| `instanceIn.conditionGroups[].conditions[].comparatorId` | string | no |  |
| `instanceIn.conditionGroups[].conditions[].value` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Emailchef API returns.

## Native endpoint

Through the native Emailchef API, this operation is `POST segments` (base URL `https://app.emailchef.com/apps/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-segment.md) for the provider-specific parameters and requirements.

