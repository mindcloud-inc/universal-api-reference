# Get Fundraiser Details with WhyDonate

## Endpoint

- **Method:** `GET`
- **Path:** `/fundraiser/get`
- **Base URL:** `https://fundraiser.whydonate.dev`
- **Official documentation:** [Get Fundraiser Details](https://helpdesk.whydonate.com/en/article/how-to-set-up-the-wordpress-donation-form-plugin-1n3ep8d/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | yes | Fundraiser slug used by WhyDonate public pages and widgets. |
| `language` | query | `string` | no | Language code passed by the WhyDonate widget when fetching fundraiser details. |
