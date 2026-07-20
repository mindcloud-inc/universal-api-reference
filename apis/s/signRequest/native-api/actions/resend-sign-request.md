# Resend SignRequest with SignRequest

## Endpoint

- **Method:** `POST`
- **Path:** `/signrequests/:uuid/resend_signrequest_email/`
- **Base URL:** `https://signrequest.com/api/v1`
- **Official documentation:** [Resend SignRequest](https://signrequest.com/api/v1/docs/#operation/signrequests_resend_signrequest_email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | UUID of the SignRequest to resend |
