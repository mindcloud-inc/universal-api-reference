# OpnForm: Update Form

Updates an existing form in OpnForm.

```
PUT https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/update-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpnForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/update-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "title": "string",
  "visibility": "string",
  "language": "string",
  "theme": "string",
  "presentationStyle": "string",
  "width": "string",
  "size": "string",
  "borderRadius": "string",
  "darkMode": "string",
  "color": "string",
  "uppercaseLabels": true,
  "noBranding": true,
  "transparentBackground": true,
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/update-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "title": "string",
    "visibility": "string",
    "language": "string",
    "theme": "string",
    "presentationStyle": "string",
    "width": "string",
    "size": "string",
    "borderRadius": "string",
    "darkMode": "string",
    "color": "string",
    "uppercaseLabels": true,
    "noBranding": true,
    "transparentBackground": true,
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Numeric ID of the form to update. |
| `title` | string | yes | Human-readable form title. |
| `visibility` | string | yes | Form visibility state. |
| `language` | string | yes | Two-letter ISO language code. |
| `theme` | string | yes | Form theme. |
| `presentationStyle` | string | yes | Form presentation style. |
| `width` | string | yes | Form width. |
| `size` | string | yes | Form size. |
| `borderRadius` | string | yes | Form border radius. |
| `darkMode` | string | yes | Dark mode setting. |
| `color` | string | yes | Primary color in hex format. |
| `uppercaseLabels` | boolean | yes | Whether labels should be uppercase. |
| `noBranding` | boolean | yes | Whether to hide OpnForm branding. |
| `transparentBackground` | boolean | yes | Whether to use a transparent background. |
| `properties` | object | yes | Complete JSON array of form blocks and fields. Do not send an empty array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "form": {},
      "message": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `form` | object |  |
| `message` | string |  |
| `type` | string |  |

## Native endpoint

Through the native OpnForm API, this operation is `PUT /open/forms/:id` (base URL `https://api.opnform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form.md) for the provider-specific parameters and requirements.

