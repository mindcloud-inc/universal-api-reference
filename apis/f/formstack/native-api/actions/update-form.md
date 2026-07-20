# Update Form with Formstack

Updates an existing form in Formstack.

## Endpoint

- **Method:** `PUT`
- **Path:** `/forms/:formId`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Update Form](https://developers.formstack.com/reference/editform-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `list<number>` | yes | The ID of the form. |
| `name` | body | `string` | no | Name of the form. |
| `template` | body | `number` | no | ID of template of the form. |
| `stockTemplate` | body | `list<string>` | no | Stock theme template code for the form. Accepted values: `berryNice`, `blueAfterglow`, `calmZigZag`, `celadonParchment`, `clean`, `confetti`, `corporateOffice`, `dark`, `duskPop`, `formstack`, `geometric`, `light`, `midnight`, `minimalism`, `oceanTide`, `peachyKeen`, `simple`. |
| `folder` | body | `number` | no | ID of the folder where the form will be moved. |
| `submitButtonTitle` | body | `string` | no | Title of submit button on live form. |
| `numberOfColumns` | body | `number` | no | Number of visible columns in the form. |
| `fieldLabelsPosition` | body | `list<string>` | no | Position where field labels are placed on the live form. Accepted values: `left`, `top`. |
| `saveSubmissionsToDatabase` | body | `boolean` | no | Flag to disable or enable submissions to be saved in the database. |
| `timezone` | body | `string` | no | Timezone of the form. |
| `language` | body | `string` | no | Language of the form. |
| `isActive` | body | `boolean` | no | Flag to make the form active or inactive. |
| `disabledMessage` | body | `string` | no | Message to show when the form is inactive. |
