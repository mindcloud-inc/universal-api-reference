# Get Validation File with ZeroBounce

Retrieves a bulk validation file from ZeroBounce.

## Endpoint

- **Method:** `GET`
- **Path:** `https://bulkapi.zerobounce.net/v2/getfile`
- **Base URL:** `https://api.zerobounce.net`
- **Official documentation:** [Get Validation File](https://www.zerobounce.net/docs/email-validation-api-quickstart/v2-get-file)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file_id` | query | `string` | yes |
| `activity_data` | query | `boolean` | no |
