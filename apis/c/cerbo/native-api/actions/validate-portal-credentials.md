# Validate Portal Credentials with Cerbo

Validates Cerbo patient portal login credentials.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/portal/validate_credentials`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Validate Portal Credentials](https://docs.cer.bo/#tag/Patient-Portal/operation/validatePortalCredentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | The patient's username that they use to login to your patient portal |
| `password` | body | `string` | yes | The patient's password that they use to login to your patient portal |
