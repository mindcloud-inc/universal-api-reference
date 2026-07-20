# Search Jobs with Detrack

Finds jobs in Detrack by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/dn/jobs/search`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Search Jobs](https://detrackapiv2.docs.apiary.io/#reference/jobs/search/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | Search filter object for jobs, matching the Detrack search body. |
