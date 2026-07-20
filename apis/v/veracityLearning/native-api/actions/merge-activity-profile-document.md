# Merge Activity Profile Document with Veracity Learning

Updates an activity profile document in Veracity Learning by merging content.

## Endpoint

- **Method:** `POST`
- **Path:** `/activities/profile`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Merge Activity Profile Document](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | query | `string` | yes | Target activity IRI. |
| `profileId` | query | `string` | yes | Exact activity profile document identifier. |
| `document` | body | `object` | yes | JSON document patch to merge into this activity profile. |
