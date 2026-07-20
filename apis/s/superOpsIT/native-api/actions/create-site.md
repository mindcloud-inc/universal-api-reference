# Create Site with SuperOps IT

## Endpoint

- **Method:** `POST`
- **Path:** `/it`
- **Base URL:** `https://api.superops.ai`
- **Official documentation:** [Create Site](https://developer.superops.com/it#mutation-createSite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The site name. |
| `working24x7` | body | `boolean` | yes | Whether the site works 24x7. |
| `timezoneCode` | body | `string` | yes | The IANA timezone code for the site. |
| `contactNumber` | body | `string` | no | The site contact number. |
