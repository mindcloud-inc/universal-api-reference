# Create Check with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/checks`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Create Check](https://docs.lob.com/#tag/Checks/operation/check_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional description for the check. |
| `to` | body | `string` | yes | Recipient address ID. |
| `from` | body | `string` | yes | Sender address ID. |
| `bank_account` | body | `string` | yes | Verified bank account ID. |
| `amount` | body | `number` | yes | US dollar amount to send. |
| `message` | body | `string` | yes | Text printed at the bottom of the check page. |
| `use_type` | body | `string` | yes | Declared mail use type. |
