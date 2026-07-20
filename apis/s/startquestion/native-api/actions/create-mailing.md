# Create Mailing with Startquestion

Creates a survey mailing in Startquestion.

## Endpoint

- **Method:** `POST`
- **Path:** `/mailing/create`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Create Mailing](https://help.startquestion.com/en/articles/5810255-mailing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_survey` | body | `number` | yes | Survey ID. |
| `id_template` | body | `number` | yes | Template ID. |
