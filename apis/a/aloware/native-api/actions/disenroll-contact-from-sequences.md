# Disenroll Contact From Sequences with Aloware

Disenrolls a contact from Aloware sequences.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhook/sequence-disenroll`
- **Base URL:** `https://app.aloware.com`
- **Official documentation:** [Disenroll Contact From Sequences](https://support.aloware.com/en/articles/9020073-aloware-sequence-api-enroll-and-disenroll-contacts-in-sequences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | body | `string` | yes | Use `phone_number` to disenroll by phone number. Otherwise provide the source system name and a Source ID. |
| `phone_number` | body | `string` | no | Phone number to disenroll when Source is `phone_number`. |
| `id` | body | `string` | no | Source record ID to disenroll when Source is not `phone_number`. |
