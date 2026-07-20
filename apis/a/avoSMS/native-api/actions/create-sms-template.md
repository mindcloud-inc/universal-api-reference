# Create SMS Template with AvoSMS

Creates a new SMS template in AvoSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/model/sms/create`
- **Base URL:** `https://api.avosms.com`
- **Official documentation:** [Create SMS Template](https://www.avosms.com/en/api/documentation/model/sms/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelContent` | body | `string` | yes | SMS template content |
| `modelName` | body | `string` | no | SMS template name |
