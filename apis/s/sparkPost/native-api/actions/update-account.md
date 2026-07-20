# Update Account with SparkPost

## Endpoint

- **Method:** `PUT`
- **Path:** `/account`
- **Base URL:** `https://api.sparkpost.com/api/v1`
- **Official documentation:** [Update Account](https://developers.sparkpost.com/api/account/#account-put-update-account-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | body | `string` | no | Company name for the account profile. |
| `options.smtp_tracking_default` | body | `boolean` | no | Whether SMTP tracking is enabled by default for the account. |
