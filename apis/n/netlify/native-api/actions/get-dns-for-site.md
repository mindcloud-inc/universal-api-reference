# Get DNS for Site with Netlify

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/dns`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Get DNS for Site](https://open-api.netlify.com/#operation/getDNSForSite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes | The Netlify site ID. |
