# List News Sources with NewsData.io

## Endpoint

- **Method:** `GET`
- **Path:** `/sources`
- **Base URL:** `https://newsdata.io/api/1`
- **Official documentation:** [List News Sources](https://newsdata.io/documentation#news-sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Category filter for source results. |
| `country` | query | `string` | no | Country code filter for source results. |
| `domainurl` | query | `string` | no | Filter sources by one or more domain URLs. |
| `language` | query | `string` | no | Language code filter for source results. |
