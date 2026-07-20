# Typeform: Update Custom Messages



```
PUT https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-custom-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-custom-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-custom-messages', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `block.dropdown.hint` | string | no |  |
| `block.dropdown.placeholder` | string | no |  |
| `block.dropdown.placeholderTouch` | string | no |  |
| `block.fileUpload.choose` | string | no |  |
| `block.fileUpload.drag` | string | no |  |
| `block.fileUpload.uploadingProgress` | string | no |  |
| `block.legal.accept` | string | no |  |
| `block.legal.reject` | string | no |  |
| `block.longtext.hint` | string | no |  |
| `block.multipleChoice.hint` | string | no |  |
| `block.multipleChoice.other` | string | no |  |
| `block.payment.cardNameTitle` | string | no | Custom message override. |
| `block.payment.cardNumberTitle` | string | no | Custom message override. |
| `block.payment.cvcDescription` | string | no | Custom message override. |
| `block.payment.cvcNumberTitle` | string | no | Custom message override. |
| `block.shortText.placeholder` | string | no | Custom message override. |
| `formId` | string | yes | Typeform form identifier. |
| `label.action.share` | string | no |  |
| `label.button.ok` | string | no |  |
| `label.button.review` | string | no |  |
| `label.button.submit` | string | no |  |
| `label.buttonHint.default` | string | no | Custom message override. |
| `label.buttonHint.longtext` | string | no | Custom message override. |
| `label.buttonNoAnswer.default` | string | no | Custom message override. |
| `label.error.emailAddress` | string | no |  |
| `label.error.expiryMonthTitle` | string | no |  |
| `label.error.expiryYearTitle` | string | no |  |
| `label.error.incompleteForm` | string | no |  |
| `label.error.maxLength` | string | no |  |
| `label.error.maxValue` | string | no |  |
| `label.error.minValue` | string | no |  |
| `label.error.mustAccept` | string | no |  |
| `label.error.mustEnter` | string | no |  |
| `label.error.mustSelect` | string | no |  |
| `label.error.range` | string | no |  |
| `label.error.required` | string | no |  |
| `label.error.server` | string | no |  |
| `label.error.sizeLimit` | string | no |  |
| `label.error.url` | string | no |  |
| `label.hint.key` | string | no |  |
| `label.no.default` | string | no |  |
| `label.no.shortcut` | string | no |  |
| `label.preview` | string | no |  |
| `label.progress.percent` | string | no |  |
| `label.progress.proportion` | string | no |  |
| `label.warning.connection` | string | no | Custom message override. |
| `label.warning.correction` | string | no | Custom message override. |
| `label.warning.fallbackAlert` | string | no |  |
| `label.warning.formUnavailable` | string | no |  |
| `label.warning.success` | string | no |  |
| `label.yes.default` | string | no |  |
| `label.yes.shortcut` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body returned when the custom messages are updated successfully. |

## Native endpoint

Through the native Typeform API, this operation is `PUT /forms/:formId/messages` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-messages.md) for the provider-specific parameters and requirements.

