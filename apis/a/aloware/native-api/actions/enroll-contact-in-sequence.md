# Enroll Contact In Sequence with Aloware

Enrolls a contact in an Aloware sequence.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhook/sequence-enroll`
- **Base URL:** `https://app.aloware.com`
- **Official documentation:** [Enroll Contact In Sequence](https://support.aloware.com/en/articles/9020073-aloware-sequence-api-enroll-and-disenroll-contacts-in-sequences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | body | `string` | yes | Use `phone_number` to enroll by phone number. Otherwise provide the source system name and a Source ID. |
| `phone_number` | body | `string` | no | Phone number to enroll when Source is `phone_number`. |
| `id` | body | `string` | no | Source record ID to enroll when Source is not `phone_number`. |
| `sequence_id` | body | `number` | yes | Numeric sequence ID to enroll the contact into. |
