# OpnForm: Create Form

Creates a new form in OpnForm.

```
POST https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpnForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "title": "string",
  "visibility": "public",
  "language": "en",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "title": "string",
    "visibility": "public",
    "language": "en",
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes | Workspace ID that will own the form. |
| `title` | string | yes | Human-readable form title. |
| `visibility` | string | yes | Form visibility state. Default: `public`. |
| `language` | string | yes | Two-letter ISO language code. Default: `en`. |
| `properties` | object | yes | JSON array of form blocks and fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "form": {},
      "message": "string",
      "type": "string",
      "usersFirstForm": true
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
| `usersFirstForm` | boolean |  |

## Native endpoint

Through the native OpnForm API, this operation is `POST /open/forms` (base URL `https://api.opnform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

