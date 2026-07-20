# Get Overall Stats with Hey Reach

Retrieves overall stats from Hey Reach.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/stats/GetOverallStats`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [Get Overall Stats](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountIds[]` | body | `array<number>` | no |
| `campaignIds[]` | body | `array<string>` | no |
| `startDate` | body | `date` | no |
| `endDate` | body | `date` | no |
