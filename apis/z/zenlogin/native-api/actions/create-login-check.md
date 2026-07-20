# Create Login Check with Zenlogin

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/[:application_key]/logins/checks`
- **Base URL:** `https://api.zenlogin.co/v1`
- **Official documentation:** [Create Login Check](https://zenlogin.co/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity_key` | body | `string` | yes | Stable unique identifier for the user being checked. Zenlogin recommends this should not be the user's email address. Maximum length is 128 characters. Maximum length: 128. |
| `identity_email_address` | body | `string` | yes | Email address Zenlogin can notify if a suspicious login is detected. Maximum length is 256 characters. Maximum length: 256. |
| `user_agent` | body | `string` | yes | User agent observed during the login attempt. Maximum length is 512 characters. Maximum length: 512. |
| `ip_address` | body | `string` | yes | IP address observed during the login attempt. Official examples use the `ip_address` payload field. Maximum length is 256 characters. Maximum length: 256. |
| `identity_first_name` | body | `string` | no | Optional first name for notification template variables. Maximum length is 256 characters. Maximum length: 256. |
| `identity_last_name` | body | `string` | no | Optional last name for notification template variables. Maximum length is 256 characters. Maximum length: 256. |
| `identity_full_name` | body | `string` | no | Optional full name for notification template variables. Maximum length is 256 characters. Maximum length: 256. |
| `req_process` | body | `number` | no | Optional 0 or 1 flag controlling whether Zenlogin should process this login check. |
