# Remove Suppressed Address with PostcardMania

Deletes an existing suppressed address from PostcardMania.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/suppression-list/{{suppressionAddressID}}`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Remove Suppressed Address](https://docs.pcmintegrations.com/docs/directmail-api/vp81vl1e1rq3t)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `suppressionAddressID` | path | `number` | yes | Suppression list entry identifier. |
