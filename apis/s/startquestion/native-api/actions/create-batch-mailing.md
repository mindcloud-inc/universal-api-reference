# Create Batch Mailing with Startquestion

Creates a survey mailing from a respondent batch in Startquestion.

## Endpoint

- **Method:** `POST`
- **Path:** `/mailing/batch`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Create Batch Mailing](https://help.startquestion.com/en/articles/5810255-mailing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | body | `string` | yes | Batch ID. |
| `template_id` | body | `number` | yes | Template ID. |
