# List Agent Profile IDs with Veracity Learning

Lists agent profile IDs from Veracity Learning.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/profile`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [List Agent Profile IDs](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent` | query | `object` | yes | Agent object whose profile ids should be listed |
| `since` | query | `date` | no | Only return profile ids updated since this timestamp |
