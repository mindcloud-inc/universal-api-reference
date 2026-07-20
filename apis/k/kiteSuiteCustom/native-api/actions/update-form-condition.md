# Update Form Condition with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/form/condition/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Form Condition](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | ID of the form condition to update. |
| `ifElement` | body | `string` | yes | ID of the element on which the condition is based. |
| `condition` | body | `string` | yes | Condition to be evaluated. |
| `target` | body | `string` | yes | Target element or field. |
| `value` | body | `string` | yes | Value to compare against (required if target is 'val'). |
| `anotherElement` | body | `string` | yes | ID of another element for comparison (required if target is 'ae'). |
| `doCondition` | body | `string` | yes | Action to perform if the condition is met (required for 'show-hide' and 'req-unreq' types). |
| `actionElements[]` | body | `array` | yes | Array of element IDs to be affected by the action (required for 'show-hide' and 'req-unreq' types). |
| `taskField` | body | `string` | yes | ID of the task field related to the condition (required if targetValue is 'ae'). |
| `targetValue` | body | `string` | yes | Target value for task field comparison. |
| `defaultElementValue` | body | `string` | yes | Default element value (required if targetValue is 'ae'). |
| `defaultValue` | body | `string` | yes | Default value (required if targetValue is 'val'). |
