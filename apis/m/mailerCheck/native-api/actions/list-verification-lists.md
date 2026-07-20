# List Verification Lists with MailerCheck

Retrieves all verification lists from MailerCheck.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists`
- **Base URL:** `https://app.mailercheck.com/api`
- **Official documentation:** [List Verification Lists](https://developers.mailercheck.com/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to request from MailerCheck. The provider did not honor limit during live verification, so page is the only published pagination control. |
