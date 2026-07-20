# Opt Out Contact from Campaign with Dripcel

Updates a contact to opt out of one Dripcel campaign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:cell/optOut`
- **Base URL:** `https://api.dripcel.com`
- **Official documentation:** [Opt Out Contact from Campaign](https://docs.dripcel.com/API/contacts#opt-out-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cell` | path | `string` | yes | — |
| `campaign_id` | body | `string` | yes | The campaign ID to opt the contact out from. |
| `all` | body | `boolean` | no | Opt the contact out from all existing and future campaigns. |
