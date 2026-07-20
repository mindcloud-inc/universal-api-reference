# Lookup Spam Score and HLR with CallerAPI

Retrieves spam score and HLR data from CallerAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/lookup/:phone`
- **Base URL:** `https://api.callerapi.com`
- **Official documentation:** [Lookup Spam Score and HLR](https://docs.callerapi.com/spam-score-hlr-19887237e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hlr` | query | `boolean` | no | Whether to include HLR data. |
| `phone` | path | `string` | yes | Phone number to look up. |
