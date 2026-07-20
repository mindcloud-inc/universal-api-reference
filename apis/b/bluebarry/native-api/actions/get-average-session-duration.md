# Get Average Session Duration with Bluebarry

Retrieves average session duration analytics from Bluebarry.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/GetAverageSessionDuration(advisorId={advisorId},questionId={questionId},startDate={startDate},endDate={endDate})`
- **Base URL:** `https://data.bluebarry.ai/`
- **Official documentation:** [Get Average Session Duration](https://data.bluebarry.ai/data/$metadata)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `advisorId` | path | `string` | yes |
| `endDate` | path | `date` | yes |
| `questionId` | path | `string` | yes |
| `startDate` | path | `date` | yes |
