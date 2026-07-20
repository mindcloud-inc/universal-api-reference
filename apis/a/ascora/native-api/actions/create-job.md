# Create Job with Ascora

Creates a new job in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Jobs/Job`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Create Job](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=53)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteCustomer.id` | body | `string` | yes | ID of the site customer associated with the job. |
| `jobName` | body | `string` | no | Name of the new job. |
| `jobDescription` | body | `string` | no | Description for the new job. |
| `pricingMethod` | body | `string` | no | Pricing method for the job. If omitted, Ascora uses the default pricing method. |
| `billingCustomer.id` | body | `string` | no | ID of the billing customer associated with the job. If omitted, Ascora uses the site's linked billing customer. |
| `completedDate` | body | `date` | no | Completion timestamp for the job. |
