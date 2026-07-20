# Get Estimate with Housecall Pro

## Endpoint

- **Method:** `GET`
- **Path:** `/estimates/:estimate_id`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [Get Estimate](https://docs.housecallpro.com/docs/housecall-public-api/eae5e9c092ef2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `estimate_id` | path | `string` | yes | Estimate identifier. |
| `expand` | query | `list<string>` | no | Array of strings to expand response body. Accepted values: `attachments`. Send multiple values as a array. |
