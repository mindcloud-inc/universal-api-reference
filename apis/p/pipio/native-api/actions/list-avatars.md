# List Avatars with Pipio

Finds available digital avatars in Pipio.

## Endpoint

- **Method:** `GET`
- **Path:** `/actor`
- **Base URL:** `https://avatar.pipio.ai`
- **Official documentation:** [List Avatars](https://docs.pipio.ai/avatar-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gender` | query | `list` | no | Filter avatars by gender. Accepted values: `female`, `male`. |
| `ages` | query | `list` | no | Filter avatars by age band. Accepted values: `middle`, `old`, `young`. |
| `ethnicities` | query | `list` | no | Filter avatars by ethnicity. Accepted values: `Asian`, `Black`, `Latino / Hispanic`, `Middle Eastern`, `South Asian / Indian`, `Southeast Asian / Pacific Island`, `White / Caucasian`. |
| `shots` | query | `list` | no | Filter avatars by shot type. Accepted values: `closeup`, `medium`. |
