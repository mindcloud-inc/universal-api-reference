# Bulk People Enrichment with Apollo

Retrieves enriched data for up to 10 people from Apollo.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/people/bulk_match`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Bulk People Enrichment](https://docs.apollo.io/reference/bulk-people-enrichment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_waterfall_email` | query | `boolean` | no | Set to true to enable email waterfall enrichment |
| `run_waterfall_phone` | query | `boolean` | no | Set to true to enable phone waterfall enrichment |
| `reveal_personal_emails` | query | `boolean` | no | Set to `true` if you want to enrich all matched people with personal emails. This potentially consumes credits as part of your Apollo pricing plan . The default value is `false`. If a person resides in a GDPR -compliant region, Apollo will not reveal their personal email. |
| `reveal_phone_number` | query | `boolean` | no | Set to `true` if you want to enrich the data of all matched people with all available phone numbers, including mobile phone numbers. This potentially consumes credits as part of your Apollo pricing plan . The default value is `false`. If this parameter is set to `true`, you must enter a webhook URL for the `webhook_url` parameter. Apollo will asynchronously verify phone numbers for you, then send a JSON response that includes only details about the phone numbers to the webhook URL you provide. It can take several minutes for the phone numbers to be delivered. |
| `webhook_url` | query | `string` | no | If you set the `reveal_phone_number` parameter to `true`, this parameter becomes mandatory. Otherwise, do not use this parameter. Enter the webhook URL that specifies where Apollo should send a JSON response that includes the phone number you requested. Apollo suggests testing this flow to ensure you receive the separate response with the phone number. If phone numbers are not revealed delivered to the webhook URL, try applying UTF-8 encoding to the webhook URL. Example: `https://webhook.site/cc4cf44e-e047-4774-8dac-473d28474e40`; `https%3A%2F%2Fwebhook.site%2Fcc4cf44e-e047-4774-8dac-473d28474e40` |
| `details[]` | body | `array<object>` | yes | Provide info for each person you want to enrich as an object within this array. Add up to 10 people. |
| `details[].first_name` | body | `string` | no | The first name of the person. This is typically used in combination with the `last_name` parameter. Example: `tim` |
| `details[].last_name` | body | `string` | no | The last name of the person. This is typically used in combination with the `first_name` parameter. Example: `zheng` |
| `details[].name` | body | `string` | no | The full name of the person. This will typically be a first name and last name separated by a space. If you use this parameter, you do not need to use the `first_name` and `last_name` parameters. Example: `tim zheng` |
| `details[].email` | body | `string` | no | The email address of the person. Example: `example@email.com` |
| `details[].hashed_email` | body | `string` | no | The hashed email of the person. The email should adhere to either the MD5 or SHA-256 hash format. Example: `8d935115b9ff4489f2d1f9249503cadf` (MD5) or `97817c0c49994eb500ad0a5e7e2d8aed51977b26424d508f66e4e8887746a152` (SHA-256) |
| `details[].organization_name` | body | `string` | no | The name of the person's employer. This can be the current employer or a previous employer. Example: `apollo` |
| `details[].domain` | body | `string` | no | The domain name for the person's employer. This can be the current employer or a previous employer. Do not include `www.`, the `@` symbol, or similar. Example: `apollo.io` or `microsoft.com` |
| `details[].id` | body | `string` | no | The Apollo ID for the person. Each person in the Apollo database is assigned a unique ID. To find IDs, call the People API Search endpoint and identify the values for `person_id`. Example: `587cf802f65125cad923a266` |
| `details[].linkedin_url` | body | `string` | no | The URL for the person's LinkedIn profile. Example: `http://www.linkedin.com/in/tim-zheng-677ba010` |
