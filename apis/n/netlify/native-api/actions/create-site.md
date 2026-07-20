# Create Site with Netlify

## Endpoint

- **Method:** `POST`
- **Path:** `/sites`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Create Site](https://open-api.netlify.com/#operation/createSite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The site name. |
| `configure_dns` | query | `boolean` | no | Whether to configure managed DNS for the new site. |
