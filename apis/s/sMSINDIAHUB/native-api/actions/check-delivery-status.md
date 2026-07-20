# Check Delivery Status with SMSINDIAHUB

Retrieves SMS delivery status from SMSINDIAHUB by message ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendorsms/checkdelivery.aspx`
- **Base URL:** `https://cloud.smsindiahub.in`
- **Official documentation:** [Check Delivery Status](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageid` | query | `string` | yes | The message ID returned by SMSINDIAHUB when the SMS was submitted. |
