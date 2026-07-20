# Issue Agreement with CoachAccountable

Issues an agreement in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Issue Agreement](https://www.coachaccountable.com/APIDocs#Agreement.issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | — |
| `AgreementTemplateID` | body | `number` | yes | The ID of the Agreement Template to issue. Can be obtained from Agreement.getTemplates |
| `title` | body | `string` | no | Allows you to specify an alternate title for the Agreement. When omitted, will default to that specified by the Agreement Template. |
