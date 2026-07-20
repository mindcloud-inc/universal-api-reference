# Reattempt Job with Detrack

Reattempts a failed job in Detrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/dn/jobs/reattempt`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Reattempt Job](https://detrackapiv2.docs.apiary.io/#reference/jobs/reattempt/reattempt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Body object sent as data with do_number and date for the job to reattempt. |
