# Weavely: Create Form

Creates a new form in Weavely.

```
POST https://connect.mindcloud.co/v1/universal/weavely/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weavely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weavely/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "formJSON": {},
  "themeJSON": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weavely/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "formJSON": {},
    "themeJSON": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Display name for the form shown in the Weavely dashboard. |
| `teamId` | string | yes | The UUID of the team to associate this form with. |
| `publish` | boolean | no | Set to true to publish the form immediately. |
| `formJSON` | object | yes | The form structure containing all pages and elements. |
| `themeJSON` | object | yes | The form visual theme configuration. |
| `settings` | object | no | Optional form settings. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logicRules[]` | array<object> | no | Optional conditional logic rules. |
| `eventTriggers[]` | array<object> | no | Optional event-based triggers. |
| `calculatedValues[]` | array<object> | no | Optional calculated field values. |
| `pageAttributes` | object | no | Optional page-specific attributes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "editor": "string",
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `editor` | string | The direct link to edit the form. |
| `id` | string | The created form unique identifier. |
| `url` | string | The direct public link to the form when published. |

## Native endpoint

Through the native Weavely API, this operation is `POST /forms` (base URL `https://api.weavely.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

