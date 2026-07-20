# Google Forms: Create Form

Creates a new empty form in Google Forms.

```
POST https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Wizard test form - 2026-03-02"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Wizard test form - 2026-03-02"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Visible title for responders. Google Forms create copies this field. Example: `Wizard test form - 2026-03-02`. |
| `documentTitle` | string | no | Optional Drive document title for the new form. Google allows this only during form creation. |
| `unpublished` | boolean | no | When true, creates the form unpublished so it does not accept responses yet. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formId": "string",
      "info": {
        "documentTitle": "string",
        "title": "string"
      },
      "publishSettings": {
        "publishState": {
          "isAcceptingResponses": true,
          "isPublished": true
        }
      },
      "responderUri": "string",
      "revisionId": "string",
      "settings": {
        "emailCollectionType": "ava@example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formId` | string |  |
| `info.documentTitle` | string |  |
| `info.title` | string |  |
| `publishSettings.publishState.isAcceptingResponses` | boolean |  |
| `publishSettings.publishState.isPublished` | boolean |  |
| `responderUri` | string |  |
| `revisionId` | string |  |
| `settings.emailCollectionType` | string |  |

## Native endpoint

Through the native Google Forms API, this operation is `POST /` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

