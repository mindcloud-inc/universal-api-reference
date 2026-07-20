# Google Forms: Get Form

Retrieves a form from Google Forms.

```
GET https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/get-form?connectionId=$CONNECTION_ID&formId=1FAIpQLSdExampleFormId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "1FAIpQLSdExampleFormId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/get-form?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form identifier. Example: `1FAIpQLSdExampleFormId`. |

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

Through the native Google Forms API, this operation is `GET /:formId` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

