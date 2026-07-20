# Update Form Field with Formstack

Updates an existing field in a Formstack form.

## Endpoint

- **Method:** `PUT`
- **Path:** `/forms/:formId/fields/:fieldId`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Update Form Field](https://developers.formstack.com/reference/editfield-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `number` | yes | The ID of the form. |
| `fieldId` | path | `number` | yes | The ID of the field. |
| `label` | body | `string` | no | Label of the field. |
| `type` | body | `list<string>` | no | Type of the field. Accepted values: `address`, `checkbox`, `creditcard`, `datetime`, `divider`, `email`, `embed`, `file`, `matrix`, `name`, `number`, `phone`, `product`, `radio`, `rating`, `richtext`, `section`, `select`, `signature`, `table`, `text`, `textarea`. |
| `internalLabel` | body | `string` | no | Internal label of the field. |
| `supportingText` | body | `string` | no | Description of the field. |
| `useCallout` | body | `boolean` | no | Show the description in a callout box. |
| `required` | body | `boolean` | no | Mark the field as required. |
| `readOnly` | body | `boolean` | no | Do not allow the field value to be changed. |
| `hidden` | body | `boolean` | no | Hide the field. |
| `unique` | body | `boolean` | no | Require a unique value for the field. |
| `hideLabel` | body | `boolean` | no | Hide the field label. |
| `columnSpan` | body | `number` | no | How many columns the field takes on the live form. |
| `language` | body | `list<string>` | no | Language of the field. Accepted values: `af`, `ar`, `bg`, `cs`, `cy`, `da`, `de`, `default`, `el`, `en`, `es`, `fi`, `fr`, `he`, `hr`, `hu`, `id`, `is`, `it`, `ja`, `kk`, `ko`, `nl`, `no`, `pl`, `pt`, `ro`, `ru`, `sk`, `sl`, `sq`, `sv`, `th`, `tr`, `vi`, `zh`, `zh-TW`. |
| `defaultValue` | body | `string` | no | Default value on the live form. |
| `options[]` | body | `array<object>` | no | Options attached to the field. |
| `smartListId` | body | `number` | no | ID of the smart list to attach. |
| `unlinkSmartList` | body | `boolean` | no | Unlink the smart list from the field. |
| `attributes` | body | `object` | no | Field attributes component. |
| `logic` | body | `object` | no | Logic for the field. |
| `numericCalculation[]` | body | `array<object>` | no | Numeric calculation definition for the field. |
| `datetimeCalculation` | body | `object` | no | Datetime calculation definition for the field. |
