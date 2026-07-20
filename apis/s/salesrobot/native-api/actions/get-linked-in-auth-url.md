# Get LinkedIn Auth URL with Salesrobot

## Endpoint

- **Method:** `POST`
- **Path:** `/api/linkedin/account/auth`
- **Base URL:** `https://api.boomtechinc.com`
- **Official documentation:** [Get LinkedIn Auth URL](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | body | `string` | yes | LinkedIn email address to onboard |
| `billAccount` | body | `boolean` | no | Whether to bill the connected LinkedIn account |
| `editAccount` | body | `boolean` | no | Whether this is an existing account edit flow |
| `timeZone` | body | `string` | yes | IANA time zone for the account |
| `domain` | body | `string` | no | Origin domain for the onboarding flow |
| `path` | body | `string` | no | Origin path for the onboarding flow |
