# Count Form Submissions with Formstack

Retrieves submission counts for a form from Formstack.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/submissions/count`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Count Form Submissions](https://developers.formstack.com/reference/countformsubmissions-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `list<number>` | yes | The ID of the form. |
| `startDate` | query | `date` | no | When to start submission count from. |
| `lookbackPeriod` | query | `number` | no | How many days to count backwards from (maximum 7). |
