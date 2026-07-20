# Create Or Update Record with MOBIDI

Creates or updates a record in MOBIDI.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiQueryManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Create Or Update Record](https://destek.dece.com.tr/space/PAR/1308524567/Mobidi+Server+Create+Update+MobidiEntry+API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entry` | body | `string` | yes | Serialized MobidiEntry payload from the official EditMobidiEntry method. |
| `OptionCheck` | body | `boolean` | no | Optional MOBIDI validation flag. |
| `ForOnlyAttachmentDelete` | body | `boolean` | no | Optional attachment-delete-only mode flag. |
