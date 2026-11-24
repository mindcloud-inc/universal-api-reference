# List Jobs with UKG Ready

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/companies/:cid/lookup/jobs`
- **Base URL:** `https://{hostname}/ta/rest`
- **Official documentation:** [List Jobs](https://secure7.saashr.com/ta/docs/rest/public)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | no | Company ID to query. Leave blank to use the company from your connection. |
