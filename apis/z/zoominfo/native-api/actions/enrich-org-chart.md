# Enrich Org Chart with Zoominfo

Enriches an org chart with ZoomInfo data.

## Endpoint

- **Method:** `POST`
- **Path:** `enrich/orgchart`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [Enrich Org Chart](https://api-docs.zoominfo.com/#763b3c10-41d1-4d52-9775-1712f712202e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `string` | no | ZoomInfo unique identifier of the company for which you want to view the org chart |
| `department` | body | `string` | no | A comma delimited string of departments to display org charts for. From this endpoint : lookup/department Send multiple values as a string separated by `,`. |
| `contactAccuracyScoreMin` | body | `string` | no | Minimum accuracy score for search results. This score indicates the likelihood that a contact is reachable and still employed by the company listed. Minimum score is 70 and maximum is 99. |
| `contactAccuracyScoreMax` | body | `string` | no | Maximum accuracy score for search results. This score indicates the likelihood that a contact is reachable and still employed by the company listed. Minimum score is 70 and maximum is 99. |
