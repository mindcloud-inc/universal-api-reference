# Create Form with Formstack

Creates a new form in Formstack.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Create Form](https://developers.formstack.com/reference/createform-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the form. |
| `template` | body | `number` | no | ID of template of the form. |
| `stockTemplate` | body | `list<string>` | no | Stock theme template code for the form. Accepted values: `berryNice`, `blueAfterglow`, `calmZigZag`, `celadonParchment`, `clean`, `confetti`, `corporateOffice`, `dark`, `duskPop`, `formstack`, `geometric`, `light`, `midnight`, `minimalism`, `oceanTide`, `peachyKeen`, `simple`. |
| `folder` | body | `number` | no | ID of the folder where the form will be created. |
| `submitButtonTitle` | body | `string` | no | Title of submit button on live form. |
| `numberOfColumns` | body | `number` | no | Number of visible columns in the form. |
| `fieldLabelsPosition` | body | `list<string>` | no | Position where field labels are placed on the live form. Accepted values: `left`, `top`. |
| `saveSubmissionsToDatabase` | body | `boolean` | no | Flag to disable or enable submissions to be saved in the database. |
| `timezone` | body | `string` | no | Timezone of the form. |
| `language` | body | `string` | no | Language of the form. |
| `isActive` | body | `boolean` | no | Flag to make the form active or inactive. |
| `disabledMessage` | body | `string` | no | Message to show when the form is inactive. |
| `fields[]` | body | `array<object>` | no | Optional fields to create with the form as raw Create Field objects. |
