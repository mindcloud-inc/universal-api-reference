# Find People with Datagma

Finds people in Datagma by company and job title.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/find_people`
- **Base URL:** `https://gateway.datagma.net/api/ingress`
- **Official documentation:** [Find People](https://datagmaapi.readme.io/reference/ingressservice_findpeople)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currentJobTitle` | query | `string` | no | Job title or title pattern to search for within the target company. |
| `domain` | query | `string` | no | Company domain used as the company input. |
| `countries` | query | `string` | no | Country filter in minimal letters, if you want to narrow the result set. |
| `fuzzy` | query | `string` | no | Set to true to broaden matching beyond exact job-title matches. |
