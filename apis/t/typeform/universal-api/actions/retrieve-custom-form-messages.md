# Typeform: Retrieve Custom Form Messages



```
GET https://connect.mindcloud.co/v1/universal/typeform/latest/actions/retrieve-custom-form-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/retrieve-custom-form-messages?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeform/latest/actions/retrieve-custom-form-messages?${params}`, {
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
| `formId` | string | yes | Typeform form identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block": {
        "dropdownHint": "string",
        "dropdownPlaceholder": "string",
        "fileUploadChoose": "string",
        "fileUploadDrag": "string",
        "fileUploadUploadingProgress": "string",
        "legalAccept": "string",
        "legalReject": "string",
        "longtextHint": "string",
        "shortTextPlaceholder": "string"
      },
      "label": {
        "buttonHintDefault": "string",
        "buttonHintLongtext": "string",
        "buttonNoAnswerDefault": "string",
        "buttonOk": "string",
        "buttonSubmit": "string",
        "errorRequired": "string",
        "noDefault": "string",
        "warningConnection": "string",
        "yesDefault": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block` | object | Custom block messages map. |
| `block.dropdownHint` | string | Dropdown hint text. |
| `block.dropdownPlaceholder` | string | Dropdown placeholder text. |
| `block.fileUploadChoose` | string | File upload choose prompt. |
| `block.fileUploadDrag` | string | File upload drag-and-drop prompt. |
| `block.fileUploadUploadingProgress` | string | File upload progress text. |
| `block.legalAccept` | string | Legal accept text. |
| `block.legalReject` | string | Legal reject text. |
| `block.longtextHint` | string | Long-text character hint. |
| `block.shortTextPlaceholder` | string | Short-text placeholder. |
| `label` | object | Custom label messages map. |
| `label.buttonHintDefault` | string | Default short-text button hint. |
| `label.buttonHintLongtext` | string | Long-text button hint. |
| `label.buttonNoAnswerDefault` | string | Default no-answer button label. |
| `label.buttonOk` | string | Ok button label. |
| `label.buttonSubmit` | string | Submit button label. |
| `label.errorRequired` | string | Required field validation message. |
| `label.noDefault` | string | Default No label. |
| `label.warningConnection` | string | Connection warning message. |
| `label.yesDefault` | string | Default Yes label. |

## Native endpoint

Through the native Typeform API, this operation is `GET /forms/:formId/messages` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-custom-form-messages.md) for the provider-specific parameters and requirements.

