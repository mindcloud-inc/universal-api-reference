# Verify Email with Gamalogic

## Endpoint

- **Method:** `GET`
- **Path:** `/emailvrf`
- **Base URL:** `https://gamalogic.com`
- **Official documentation:** [Verify Email](https://docs.gamalogic.com/emails/verify-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailid` | query | `string` | yes | Email address to validate. |
| `speed_rank` | query | `number` | no | Optional speed and accuracy setting. Defaults to 0; higher values are slower and more accurate. |
