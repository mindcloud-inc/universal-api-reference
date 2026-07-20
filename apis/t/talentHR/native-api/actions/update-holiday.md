# Update Holiday with TalentHR

Updates an existing holiday in TalentHR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/holidays/:objectId`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [Update Holiday](https://apidocs.talenthr.io/#01e85519-8c14-42c5-b073-7f5fa46aa5e2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectId` | path | `number` | yes | TalentHR holiday ID. |
| `name` | body | `string` | yes | Holiday name. |
| `holiday_date` | body | `string` | yes | Holiday date in YYYY-MM-DD format. |
| `required_for_all` | body | `boolean` | yes | Whether the holiday applies to all employees. |
