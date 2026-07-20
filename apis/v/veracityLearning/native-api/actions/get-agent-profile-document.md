# Get Agent Profile Document with Veracity Learning

Retrieves an agent profile document from Veracity Learning.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/profile`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Get Agent Profile Document](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent` | query | `object` | yes | Agent object whose profile document should be loaded |
| `profileId` | query | `string` | yes | Profile id to load |
