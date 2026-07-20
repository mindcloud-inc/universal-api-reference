# Print Survey with SmartSurvey

Renders a SmartSurvey survey as HTML, Word, or PDF.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/print`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Print Survey](https://docs.smartsurvey.io/reference/get_surveys-surveyid-print)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id of the survey you want to print |
| `t` | query | `number` | yes | The output type you want to print the survey as.  Options: 1: Word doc \| 2: HTML \| 3: PDF |
| `st` | query | `number` | no | The survey translation id to print the survey in. |
| `dst` | query | `boolean` | no | Whether to include the title of the survey. (default: true) |
| `dsl` | query | `boolean` | no | Whether to include the logo. (default: true) |
| `qn` | query | `boolean` | no | Whether to include question numbers. (default: true) |
| `pn` | query | `boolean` | no | Whether to include page numbers. (default: true) |
| `pt` | query | `boolean` | no | Whether to include page headings. (default: true) |
| `pd` | query | `boolean` | no | Whether to include page descriptions. (default: true) |
| `pb` | query | `boolean` | no | Whether to include page breaks. (default: true) |
| `pqb` | query | `boolean` | no | Whether to prevent breaking questions across pages. (default: true) |
| `qf` | query | `boolean` | no | Whether to strip HTML tags from all questions. (default: false) |
| `of` | query | `boolean` | no | Whether to strip HTML tags from all answer choices. (default: false) |
| `stbg` | query | `string` | no | The background color of the survey title. (default: #1170a8 - dark blue) |
| `stc` | query | `string` | no | The color of the survey title text. (default: #FFFFFF - white) |
| `slbg` | query | `string` | no | The background color of the survey logo. (default: #FFFFFF - white) |
| `ptbg` | query | `string` | no | The background color of the page title. (default: #424242 - dark gray/black) |
| `ptc` | query | `string` | no | The color of the page title text. (default: #FFFFFF - white) |
