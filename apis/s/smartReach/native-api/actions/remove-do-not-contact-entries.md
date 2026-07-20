# Remove Do Not Contact Entries with SmartReach

Deletes do not contact entries from SmartReach.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/do_not_contact`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [Remove Do Not Contact Entries](https://help.smartreach.io/reference/deletednc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dnc_ids[]` | body | `array<string>` | no | Ids of do_not_contact to be deleted |
