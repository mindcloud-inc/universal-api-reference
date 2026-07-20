# Create Consent with iubenda

Creates a consent in iubenda.

## Endpoint

- **Method:** `POST`
- **Path:** `/consent`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [Create Consent](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#consent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `object` | no | Subject data for the consent event. |
| `subject.id` | body | `string` | no | Subject ID for the consent event. |
| `subject.email` | body | `string` | no | Subject email address for the consent event. |
| `subject.first_name` | body | `string` | no | Subject first name for the consent event. |
| `subject.last_name` | body | `string` | no | Subject last name for the consent event. |
| `subject.full_name` | body | `string` | no | Subject full name for the consent event. |
| `subject.verified` | body | `boolean` | no | Whether the consent subject is verified. |
| `subject.phones[]` | body | `array<object>` | no | Array of phone objects for the consent subject. |
| `subject.phones[].number` | body | `string` | no | A phone number with country code prefix for the consent subject. |
| `subject.phones[].label` | body | `string` | no | Label used to identify the consent subject phone number. |
| `legal_notices[]` | body | `array<object>` | no | Legal notices associated with the consent. |
| `legal_notices[].identifier` | body | `string` | no | Identifier of a legal notice associated with the consent. |
| `legal_notices[].version` | body | `string` | no | Version of the associated legal notice. Auto-filled by iubenda when omitted. |
| `proofs[]` | body | `array<object>` | no | Proof entries associated with the consent. |
| `proofs[].content` | body | `string` | no | Proof content for the consent. |
| `proofs[].form` | body | `string` | no | Proof form for the consent. |
| `proof_document_ids[]` | body | `array<string>` | no | IDs of documents that provide proof of the consent. |
| `preferences` | body | `object` | no | Consent preference values keyed by preference name. |
| `ip_address` | body | `string` | no | IP address associated with the consent event. |
| `timestamp` | body | `string` | no | ISO 8601 timestamp at which the consent occurred. |
