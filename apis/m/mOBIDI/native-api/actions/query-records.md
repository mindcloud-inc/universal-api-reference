# Query Records with MOBIDI

Retrieves records from a MOBIDI query.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiQueryManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Query Records](https://destek.dece.com.tr/space/PAR/1308590081/Mobidi+Server+Query+API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queryObject` | body | `string` | yes | Serialized MobidiQuery payload. |
