# Update Or Delete Saved Query with MOBIDI

Updates or deletes a saved query in MOBIDI.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiQueryManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Update Or Delete Saved Query](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queryObject` | body | `string` | yes | Serialized MobidiQuery payload. |
| `queryName` | body | `string` | yes | Saved query display name. |
| `IdSavedMobidiQuery` | body | `string` | yes | Saved query identifier to update or delete. |
