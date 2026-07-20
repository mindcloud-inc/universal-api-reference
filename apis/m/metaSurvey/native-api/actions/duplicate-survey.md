# Duplicate Survey with MetaSurvey

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/survey/:surveyId/duplicate`
- **Base URL:** `https://api.getmetasurvey.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `string` | yes | Survey to duplicate. |
| `folderId` | body | `string` | yes | Folder that should own the duplicated survey. |
