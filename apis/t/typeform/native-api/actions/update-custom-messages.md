# Update Custom Messages with Typeform

## Endpoint

- **Method:** `PUT`
- **Path:** `/forms/:formId/messages`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Update Custom Messages](https://www.typeform.com/developers/create/reference/update-custom-messages/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `block.dropdown.hint` | body | `string` | no | — |
| `block.dropdown.placeholder` | body | `string` | no | — |
| `block.dropdown.placeholderTouch` | body | `string` | no | — |
| `block.fileUpload.choose` | body | `string` | no | — |
| `block.fileUpload.drag` | body | `string` | no | — |
| `block.fileUpload.uploadingProgress` | body | `string` | no | — |
| `block.legal.accept` | body | `string` | no | — |
| `block.legal.reject` | body | `string` | no | — |
| `block.longtext.hint` | body | `string` | no | — |
| `block.multipleChoice.hint` | body | `string` | no | — |
| `block.multipleChoice.other` | body | `string` | no | — |
| `block.payment.cardNameTitle` | body | `string` | no | Custom message override. |
| `block.payment.cardNumberTitle` | body | `string` | no | Custom message override. |
| `block.payment.cvcDescription` | body | `string` | no | Custom message override. |
| `block.payment.cvcNumberTitle` | body | `string` | no | Custom message override. |
| `block.shortText.placeholder` | body | `string` | no | Custom message override. |
| `formId` | path | `string` | yes | Typeform form identifier. |
| `label.action.share` | body | `string` | no | — |
| `label.button.ok` | body | `string` | no | — |
| `label.button.review` | body | `string` | no | — |
| `label.button.submit` | body | `string` | no | — |
| `label.buttonHint.default` | body | `string` | no | Custom message override. |
| `label.buttonHint.longtext` | body | `string` | no | Custom message override. |
| `label.buttonNoAnswer.default` | body | `string` | no | Custom message override. |
| `label.error.emailAddress` | body | `string` | no | — |
| `label.error.expiryMonthTitle` | body | `string` | no | — |
| `label.error.expiryYearTitle` | body | `string` | no | — |
| `label.error.incompleteForm` | body | `string` | no | — |
| `label.error.maxLength` | body | `string` | no | — |
| `label.error.maxValue` | body | `string` | no | — |
| `label.error.minValue` | body | `string` | no | — |
| `label.error.mustAccept` | body | `string` | no | — |
| `label.error.mustEnter` | body | `string` | no | — |
| `label.error.mustSelect` | body | `string` | no | — |
| `label.error.range` | body | `string` | no | — |
| `label.error.required` | body | `string` | no | — |
| `label.error.server` | body | `string` | no | — |
| `label.error.sizeLimit` | body | `string` | no | — |
| `label.error.url` | body | `string` | no | — |
| `label.hint.key` | body | `string` | no | — |
| `label.no.default` | body | `string` | no | — |
| `label.no.shortcut` | body | `string` | no | — |
| `label.preview` | body | `string` | no | — |
| `label.progress.percent` | body | `string` | no | — |
| `label.progress.proportion` | body | `string` | no | — |
| `label.warning.connection` | body | `string` | no | Custom message override. |
| `label.warning.correction` | body | `string` | no | Custom message override. |
| `label.warning.fallbackAlert` | body | `string` | no | — |
| `label.warning.formUnavailable` | body | `string` | no | — |
| `label.warning.success` | body | `string` | no | — |
| `label.yes.default` | body | `string` | no | — |
| `label.yes.shortcut` | body | `string` | no | — |
