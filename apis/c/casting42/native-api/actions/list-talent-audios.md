# List Talent Audios with Casting42

Retrieves audio files for a Casting42 talent.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/talents/audios/{{talentTag}}`
- **Base URL:** `https://casting42.com`
- **Official documentation:** [List Talent Audios](https://documenter.getpostman.com/view/24607394/2s9YR6buRP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `talentTag` | path | `string` | yes | Unique tag of the talent whose audio files you want to fetch. |
