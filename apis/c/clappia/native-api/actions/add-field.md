# Add Field with Clappia

Creates a new app field in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/appdefinitionv2/addField`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Add Field](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `sectionIndex` | body | `number` | yes | Zero-based section index where the field should be inserted. |
| `fieldIndex` | body | `number` | yes | Zero-based insertion index for the field inside the section. |
| `fieldType` | body | `string` | yes | Clappia field type to create, such as singleSelector. |
| `label` | body | `string` | yes | Field label shown to users. |
| `description` | body | `string` | no | Optional helper text for the field. |
| `required` | body | `boolean` | no | Whether the field must be filled in. |
| `blockWidthPercentageDesktop` | body | `number` | no | Desktop width percentage for the field block. |
| `blockWidthPercentageMobile` | body | `number` | no | Mobile width percentage for the field block. |
| `options[]` | body | `array<string>` | no | Selectable values for option-based field types. |
| `style` | body | `string` | no | Display style for supported field types, such as Standard or Chips. |
| `numberOfCols` | body | `number` | no | Column count for option display layouts. |
| `isEditable` | body | `boolean` | no | Whether users can edit the field. |
| `retainValues` | body | `boolean` | no | Whether field values should be retained when relevant form structure changes. |
