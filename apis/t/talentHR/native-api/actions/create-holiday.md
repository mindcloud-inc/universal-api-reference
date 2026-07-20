# Create Holiday with TalentHR

Creates a new holiday in TalentHR.

## Endpoint

- **Method:** `POST`
- **Path:** `/holidays`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [Create Holiday](https://apidocs.talenthr.io/#b837d318-676b-4647-87a0-369c0870206a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Holiday name. |
| `holiday_date` | body | `string` | yes | Holiday date in YYYY-MM-DD format. |
| `required_for_all` | body | `boolean` | yes | Whether the holiday applies to all employees. |
