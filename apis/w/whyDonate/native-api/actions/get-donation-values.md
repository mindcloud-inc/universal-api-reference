# Get Donation Values with WhyDonate

## Endpoint

- **Method:** `GET`
- **Path:** `/fundraiser/donation/values`
- **Base URL:** `https://fundraiser.whydonate.dev`
- **Official documentation:** [Get Donation Values](https://helpdesk.whydonate.com/en/article/how-to-set-up-the-wordpress-donation-form-plugin-1n3ep8d/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | yes | Fundraiser slug used to fetch donation values. |
| `currency` | query | `string` | yes | Explicit fundraiser currency code, for example eur. Runtime validation showed the endpoint succeeds with eur and fails with the old def fallback. |
