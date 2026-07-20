# Delete Sender with AvoSMS

Deletes an existing sender from AvoSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sender/delete`
- **Base URL:** `https://api.avosms.com`
- **Official documentation:** [Delete Sender](https://www.avosms.com/en/api/documentation/sender/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sender` | body | `string` | yes | Sender name between 3 and 11 characters |
