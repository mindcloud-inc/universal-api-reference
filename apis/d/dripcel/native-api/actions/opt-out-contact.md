# Opt Out Contact with Dripcel

Updates a contact to opt out of multiple Dripcel campaigns.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:cell/optOut`
- **Base URL:** `https://api.dripcel.com`
- **Official documentation:** [Opt Out Contact](https://docs.dripcel.com/API/contacts#opt-out-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cell` | path | `string` | yes | — |
| `all` | body | `boolean` | no | Opt the contact out from all existing and future campaigns. |
| `campaign_ids[]` | body | `array<string>` | no | The campaign IDs to opt the contact out from. |
| `create_missing_contact` | body | `boolean` | no | Create the contact if it does not exist before applying the opt-out. |
