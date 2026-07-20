# Update Form Design with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/form-design/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Form Design](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Form Design ID to update |
| `body` | body | `object` | yes | Request body |
| `previousNav` | body | `object` | yes | — |
| `nextNav` | body | `object` | yes | — |
| `color` | body | `object` | yes | — |
| `pageImage` | body | `object` | yes | — |
| `formImage` | body | `object` | yes | — |
| `formStyle` | body | `object` | yes | — |
| `submitButtom` | body | `object` | yes | — |
| `elementDesign` | body | `object` | yes | — |
| `formDesignTemplate` | body | `string` | yes | ID of the form design template to apply |
| `header` | body | `object` | yes | Header styling properties |
| `button` | body | `object` | yes | Button styling properties |
| `dropdown` | body | `object` | yes | Dropdown styling properties |
| `checkBox` | body | `object` | yes | Checkbox styling properties |
| `textElement` | body | `object` | yes | Text element styling properties |
| `custom` | body | `object` | yes | Custom styling properties |
