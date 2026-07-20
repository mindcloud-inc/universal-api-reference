# Formstack: Update Form Field

Updates an existing field in a Formstack form.

```
PUT https://connect.mindcloud.co/v1/universal/formstack/latest/actions/update-form-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/update-form-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "6457226",
  "fieldId": "193364423"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstack/latest/actions/update-form-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "6457226",
    "fieldId": "193364423"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | number | yes | The ID of the form. Example: `6457226`. |
| `fieldId` | number | yes | The ID of the field. Example: `193364423`. |
| `label` | string | no | Label of the field. Example: `Batch C updated field`. |
| `type` | list<string> | no | Type of the field. One of: `address`, `checkbox`, `creditcard`, `datetime`, `divider`, `email`, `embed`, `file`, `matrix`, `name`, `number`, `phone`, `product`, `radio`, `rating`, `richtext`, `section`, `select`, `signature`, `table`, `text`, `textarea`. Default: `text`. |
| `supportingText` | string | no | Description of the field. Example: `Updated during Batch C validation`. |
| `required` | boolean | no | Mark the field as required. |
| `defaultValue` | string | no | Default value on the live form. Example: `Updated value`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `internalLabel` | string | no | Internal label of the field. Example: `batch_c_updated_field`. |
| `useCallout` | boolean | no | Show the description in a callout box. |
| `readOnly` | boolean | no | Do not allow the field value to be changed. |
| `hidden` | boolean | no | Hide the field. |
| `unique` | boolean | no | Require a unique value for the field. |
| `hideLabel` | boolean | no | Hide the field label. |
| `columnSpan` | number | no | How many columns the field takes on the live form. Example: `1`. |
| `language` | list<string> | no | Language of the field. One of: `af`, `ar`, `bg`, `cs`, `cy`, `da`, `de`, `default`, `el`, `en`, `es`, `fi`, `fr`, `he`, `hr`, `hu`, `id`, `is`, `it`, `ja`, `kk`, `ko`, `nl`, `no`, `pl`, `pt`, `ro`, `ru`, `sk`, `sl`, `sq`, `sv`, `th`, `tr`, `vi`, `zh`, `zh-TW`. Example: `default`. |
| `options[]` | array<object> | no | Options attached to the field. Example: `[object Object]`. |
| `smartListId` | number | no | ID of the smart list to attach. Example: `123`. |
| `unlinkSmartList` | boolean | no | Unlink the smart list from the field. |
| `attributes` | object | no | Field attributes component. Example: `[object Object]`. |
| `logic` | object | no | Logic for the field. Example: `[object Object]`. |
| `numericCalculation[]` | array<object> | no | Numeric calculation definition for the field. Example: `[object Object]`. |
| `datetimeCalculation` | object | no | Datetime calculation definition for the field. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "confirmationText": "string",
        "hideInputCharacters": true,
        "maxLength": 1,
        "minLength": 1,
        "placeholder": "string",
        "removeDataFromEmailsAndExports": true,
        "requireConfirmation": true,
        "restrictDataAccess": true
      },
      "columnSpan": 1,
      "defaultValue": "string",
      "displayOrder": 1,
      "hidden": true,
      "hideLabel": true,
      "id": 1,
      "label": "string",
      "labelKey": "string",
      "language": "string",
      "readOnly": true,
      "required": true,
      "supportingText": "string",
      "type": "string",
      "unique": true,
      "useCallout": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.confirmationText` | string |  |
| `attributes.hideInputCharacters` | boolean |  |
| `attributes.maxLength` | number |  |
| `attributes.minLength` | number |  |
| `attributes.placeholder` | string |  |
| `attributes.removeDataFromEmailsAndExports` | boolean |  |
| `attributes.requireConfirmation` | boolean |  |
| `attributes.restrictDataAccess` | boolean |  |
| `columnSpan` | number |  |
| `defaultValue` | string |  |
| `displayOrder` | number |  |
| `hidden` | boolean |  |
| `hideLabel` | boolean |  |
| `id` | number |  |
| `label` | string |  |
| `labelKey` | string |  |
| `language` | string |  |
| `readOnly` | boolean |  |
| `required` | boolean |  |
| `supportingText` | string |  |
| `type` | string |  |
| `unique` | boolean |  |
| `useCallout` | boolean |  |

## Native endpoint

Through the native Formstack API, this operation is `PUT /forms/:formId/fields/:fieldId` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-field.md) for the provider-specific parameters and requirements.

