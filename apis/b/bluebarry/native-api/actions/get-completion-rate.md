# Get Completion Rate with Bluebarry

Retrieves completion rate analytics from Bluebarry.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/GetCompletionRate(advisorId={advisorId},questionId={questionId},startDate={startDate},endDate={endDate})`
- **Base URL:** `https://data.bluebarry.ai/`
- **Official documentation:** [Get Completion Rate](https://data.bluebarry.ai/data/$metadata)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `advisorId` | path | `string` | yes |
| `endDate` | path | `date` | yes |
| `questionId` | path | `string` | yes |
| `startDate` | path | `date` | yes |
