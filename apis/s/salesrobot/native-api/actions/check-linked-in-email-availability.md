# Check LinkedIn Email Availability with Salesrobot

## Endpoint

- **Method:** `POST`
- **Path:** `/api/linkedin_account/check_email`
- **Base URL:** `https://api.boomtechinc.com`
- **Official documentation:** [Check LinkedIn Email Availability](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | body | `string` | yes | LinkedIn email address to check |
| `editAccount` | body | `boolean` | no | Whether this is an existing account edit flow |
