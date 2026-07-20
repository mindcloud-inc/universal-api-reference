# Force Carry Forward Last Option with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/question/updateQuestion`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Force Carry Forward Last Option](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey containing the target question. |
| `questionId` | body | `string` | yes | Question receiving carried-forward answers. |
