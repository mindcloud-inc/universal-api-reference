# Get Advised Revenue Analytics with Bluebarry

Retrieves advised revenue analytics from Bluebarry.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/GetAdvisedRevenueAnalytics(advisorId={advisorId},questionId={questionId},startDate={startDate},endDate={endDate})`
- **Base URL:** `https://data.bluebarry.ai/`
- **Official documentation:** [Get Advised Revenue Analytics](https://data.bluebarry.ai/data/$metadata)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `advisorId` | path | `string` | yes |
| `endDate` | path | `date` | yes |
| `questionId` | path | `string` | yes |
| `startDate` | path | `date` | yes |
