# Kite Suite: Update Form Condition



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-condition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-condition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "id": "string",
  "ifElement": "string",
  "condition": "string",
  "target": "string",
  "value": "string",
  "anotherElement": "string",
  "doCondition": "string",
  "actionElements[]": [
    "string"
  ],
  "taskField": "string",
  "targetValue": "string",
  "defaultElementValue": "string",
  "defaultValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-condition', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "id": "string",
    "ifElement": "string",
    "condition": "string",
    "target": "string",
    "value": "string",
    "anotherElement": "string",
    "doCondition": "string",
    "actionElements[]": ["string"],
    "taskField": "string",
    "targetValue": "string",
    "defaultElementValue": "string",
    "defaultValue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | yes | ID of the form condition to update. |
| `ifElement` | string | yes | ID of the element on which the condition is based. |
| `condition` | string | yes | Condition to be evaluated. |
| `target` | string | yes | Target element or field. |
| `value` | string | yes | Value to compare against (required if target is 'val'). |
| `anotherElement` | string | yes | ID of another element for comparison (required if target is 'ae'). |
| `doCondition` | string | yes | Action to perform if the condition is met (required for 'show-hide' and 'req-unreq' types). |
| `actionElements[]` | array | yes | Array of element IDs to be affected by the action (required for 'show-hide' and 'req-unreq' types). |
| `taskField` | string | yes | ID of the task field related to the condition (required if targetValue is 'ae'). |
| `targetValue` | string | yes | Target value for task field comparison. |
| `defaultElementValue` | string | yes | Default element value (required if targetValue is 'ae'). |
| `defaultValue` | string | yes | Default value (required if targetValue is 'val'). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Updated form condition object. |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/form/condition/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-condition.md) for the provider-specific parameters and requirements.

