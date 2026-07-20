# Add Subscriber to Sequence with Kit

Adds an existing subscriber to a Kit sequence.

## Endpoint

- **Method:** `POST`
- **Path:** `/sequences/:sequence_id/subscribers`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [Add Subscriber to Sequence](https://developers.kit.com/api-reference/sequences/add-subscriber-to-sequence-by-email-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sequence_id` | path | `number` | yes | The ID of the sequence to add the subscriber to. |
| `email_address` | body | `string` | yes | Email address of an existing subscriber. |
