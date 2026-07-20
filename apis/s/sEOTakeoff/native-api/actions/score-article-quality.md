# Score Article Quality with SEOTakeoff

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/quality/score`
- **Base URL:** `https://api.seotakeoff.com`
- **Official documentation:** [Score Article Quality](https://api.seotakeoff.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Article content to score. |
| `metadata` | body | `object` | no | Optional metadata object to include with scoring. |
