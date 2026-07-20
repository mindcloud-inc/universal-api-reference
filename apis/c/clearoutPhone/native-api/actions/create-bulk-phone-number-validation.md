# Create Bulk Phone Number Validation with ClearoutPhone

Creates a bulk phone number validation job in ClearoutPhone.

## Endpoint

- **Method:** `POST`
- **Path:** `/phonenumber/bulk`
- **Base URL:** `https://api.clearoutphone.io/v1`
- **Official documentation:** [Create Bulk Phone Number Validation](https://docs.clearoutphone.io/#api-Phone_Number_Validation_API-BulkPhoneValidate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | CSV or XLSX file to upload for bulk validation |
| `country_code` | body | `string` | no | Default country code for rows without an explicit country code |
