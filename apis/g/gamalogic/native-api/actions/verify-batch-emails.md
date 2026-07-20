# Verify Batch Emails with Gamalogic

## Endpoint

- **Method:** `POST`
- **Path:** `/batchemailvrf`
- **Base URL:** `https://gamalogic.com`
- **Official documentation:** [Verify Batch Emails](https://docs.gamalogic.com/emails/verify-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gamalogic_emailid_vrfy[]` | body | `array<object>` | yes | Email records to validate. Each item should include an emailid value. |
| `speed_rank` | query | `number` | no | Optional speed and accuracy setting. Defaults to 0; higher values are slower and more accurate. |
