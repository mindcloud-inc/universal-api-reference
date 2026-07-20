# Weavely: Update Form

Updates an existing form in Weavely.

```
PUT https://connect.mindcloud.co/v1/universal/weavely/latest/actions/update-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weavely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weavely/latest/actions/update-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weavely/latest/actions/update-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique identifier of the form to update. |
| `name` | string | no | Update the form name. |
| `formJSON` | object | no | Update the form structure containing pages and elements. |
| `themeJSON` | object | no | Update the form visual theme configuration. |
| `settings` | object | no | Update form settings. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logicRules[]` | array<object> | no | Update conditional logic rules. |
| `eventTriggers[]` | array<object> | no | Update event-based triggers. |
| `calculatedValues[]` | array<object> | no | Update calculated field values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The updated form unique identifier. |

## Native endpoint

Through the native Weavely API, this operation is `POST /forms/:id` (base URL `https://api.weavely.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form.md) for the provider-specific parameters and requirements.

