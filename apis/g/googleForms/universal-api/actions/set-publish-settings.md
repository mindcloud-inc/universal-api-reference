# Google Forms: Set Publish Settings

Updates a form's publish settings in Google Forms.

```
PUT https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/set-publish-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/set-publish-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "publishState": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/set-publish-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "publishState": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form identifier. |
| `publishState` | list | yes | Publish or unpublish the form. One of: `0`, `1`. |
| `acceptingResponses` | boolean | no | Whether the published form accepts responses. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateMask` | string | no | Advanced: publish settings field mask. Defaults to publishState. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formId": "string",
      "publishSettings": {
        "publishState": {
          "isAcceptingResponses": true,
          "isPublished": true
        }
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
| `publishSettings.publishState.isAcceptingResponses` | boolean |  |
| `publishSettings.publishState.isPublished` | boolean |  |

## Native endpoint

Through the native Google Forms API, this operation is `POST /:formId:setPublishSettings` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-publish-settings.md) for the provider-specific parameters and requirements.

