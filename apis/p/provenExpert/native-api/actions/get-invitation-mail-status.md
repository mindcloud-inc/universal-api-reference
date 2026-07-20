# Get Invitation Mail Status with ProvenExpert

Retrieves the status of an invitation mailing in ProvenExpert.

## Endpoint

- **Method:** `POST`
- **Path:** `/invite/mail/status`
- **Base URL:** `https://www.provenexpert.com/api/v1`
- **Official documentation:** [Get Invitation Mail Status](https://developer.provenexpert.com/index_en.html#invite-mail-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.id` | body | `string` | yes | ID of the invitation mailing returned by Create Invitation Mail. |
