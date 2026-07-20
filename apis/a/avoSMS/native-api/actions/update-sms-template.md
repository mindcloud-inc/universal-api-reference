# Update SMS Template with AvoSMS

Updates an existing SMS template in AvoSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/model/sms/update`
- **Base URL:** `https://api.avosms.com`
- **Official documentation:** [Update SMS Template](https://www.avosms.com/en/api/documentation/model/sms/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | body | `string` | yes | SMS template ID |
| `modelName` | body | `string` | yes | SMS template name |
| `modelContent` | body | `string` | yes | SMS template content |
