# Kite Suite: Update Form Design



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-design
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-design" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "body": {},
  "previousNav": {},
  "nextNav": {},
  "color": {},
  "pageImage": {},
  "formImage": {},
  "formStyle": {},
  "submitButtom": {},
  "elementDesign": {},
  "formDesignTemplate": "string",
  "header": {},
  "button": {},
  "dropdown": {},
  "checkBox": {},
  "textElement": {},
  "custom": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-design', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "body": {},
    "previousNav": {},
    "nextNav": {},
    "color": {},
    "pageImage": {},
    "formImage": {},
    "formStyle": {},
    "submitButtom": {},
    "elementDesign": {},
    "formDesignTemplate": "string",
    "header": {},
    "button": {},
    "dropdown": {},
    "checkBox": {},
    "textElement": {},
    "custom": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Form Design ID to update |
| `body` | object | yes | Request body |
| `previousNav` | object | yes |  |
| `nextNav` | object | yes |  |
| `color` | object | yes |  |
| `pageImage` | object | yes |  |
| `formImage` | object | yes |  |
| `formStyle` | object | yes |  |
| `submitButtom` | object | yes |  |
| `elementDesign` | object | yes |  |
| `formDesignTemplate` | string | yes | ID of the form design template to apply |
| `header` | object | yes | Header styling properties |
| `button` | object | yes | Button styling properties |
| `dropdown` | object | yes | Dropdown styling properties |
| `checkBox` | object | yes | Checkbox styling properties |
| `textElement` | object | yes | Text element styling properties |
| `custom` | object | yes | Custom styling properties |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kite Suite API returns.

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/form-design/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-design.md) for the provider-specific parameters and requirements.

