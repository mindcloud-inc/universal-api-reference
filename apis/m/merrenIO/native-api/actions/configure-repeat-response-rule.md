# Configure Repeat Response Rule with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/survey/saveRecurringSurveyDetails`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Configure Repeat Response Rule](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey to configure. |
| `isRecurring` | body | `boolean` | yes | Whether repeat responses are enabled. |
| `repeatType` | body | `string` | yes | Recurring rule type, such as daily or weekly. |
