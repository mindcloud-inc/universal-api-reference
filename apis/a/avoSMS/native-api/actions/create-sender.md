# Create Sender with AvoSMS

Creates a new sender in AvoSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sender/create`
- **Base URL:** `https://api.avosms.com`
- **Official documentation:** [Create Sender](https://www.avosms.com/en/api/documentation/sender/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sender` | body | `string` | yes | Sender name between 3 and 11 characters |
