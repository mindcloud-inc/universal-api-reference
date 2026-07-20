# Create new Custom Field with Qase

Creates a new custom field in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/custom_field`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create new Custom Field](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Required request field title. |
| `entity` | body | `number` | yes | Possible values: 0 - case; 1 - run; 2 - defect; |
| `type` | body | `number` | yes | Possible values: 0 - number; 1 - string; 2 - text; 3 - selectbox; 4 - checkbox; 5 - radio; 6 - multiselect; 7 - url; 8 - user; 9 - datetime; |
