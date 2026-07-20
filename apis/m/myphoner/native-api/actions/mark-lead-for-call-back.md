# Mark Lead for Call Back with Myphoner

Marks a lead for call back in Myphoner.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/:leadId/call_back`
- **Base URL:** `https://{subdomain}.myphoner.com/api/v2`
- **Official documentation:** [Mark Lead for Call Back](https://www.myphoner.com/docs/api/#leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_back_in` | body | `number` | no | Minutes until the scheduled call back. |
| `category` | body | `string` | no | Existing Myphoner category to apply exactly as named. |
| `comment` | body | `string` | no | Comment text to attach to the lead event. |
| `leadId` | path | `number` | yes | The Myphoner lead ID. |
| `scheduled_for` | body | `date` | no | UTC datetime for the scheduled call back. Takes precedence over Call Back In when present. |
