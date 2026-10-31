# Bridgit Bench: Set Project Fields



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/set-project-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/set-project-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "payload[]": [
    {}
  ],
  "payload[].id": 1,
  "payload[].name": "Ava Chen",
  "payload[].type": "Address",
  "payload[].definedValues[].valueId": 1,
  "payload[].definedValues[].definedValue": "string",
  "payload[].definedValues[].forRemoval": true,
  "payload[].definedValues[].deleteExperienceFieldValues": true,
  "payload[].isRequired": true,
  "payload[].isPrivate": true,
  "payload[].isLocked": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/set-project-fields', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "payload[]": [{}],
    "payload[].id": 1,
    "payload[].name": "Ava Chen",
    "payload[].type": "Address",
    "payload[].definedValues[].valueId": 1,
    "payload[].definedValues[].definedValue": "string",
    "payload[].definedValues[].forRemoval": true,
    "payload[].definedValues[].deleteExperienceFieldValues": true,
    "payload[].isRequired": true,
    "payload[].isPrivate": true,
    "payload[].isLocked": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Account ID |
| `payload[]` | array<object> | yes |  |
| `payload[].id` | number | yes |  |
| `payload[].name` | string | yes |  |
| `payload[].type` | list<string> | yes | One of: `Address`, `Boolean`, `Currency`, `Date`, `Email`, `Image`, `Integer`, `LongText`, `MultiSelect`, `Number`, `Phone`, `SingleSelect`, `Text`. |
| `payload[].definedValues[]` | array<object> | no |  |
| `payload[].definedValues[].valueId` | number | yes |  |
| `payload[].definedValues[].definedValue` | string | yes |  |
| `payload[].definedValues[].forRemoval` | boolean | yes |  |
| `payload[].definedValues[].deleteExperienceFieldValues` | boolean | yes |  |
| `payload[].definedValues[].isHidden` | boolean | no | Null or omitted leaves the stored state unchanged. |
| `payload[].isRequired` | boolean | yes |  |
| `payload[].isPrivate` | boolean | yes |  |
| `payload[].isLocked` | boolean | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload[].definedValues[].parentId` | number | no | Id of the parent defined value for title hierarchy. Null or omitted leaves the stored parent unchanged; send 0 to clear it (make the value a root). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:id/project-fields` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-project-fields.md) for the provider-specific parameters and requirements.

