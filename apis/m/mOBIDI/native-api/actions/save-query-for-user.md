# Save Query For User with MOBIDI

Saves a query for a MOBIDI user.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiQueryManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Save Query For User](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queryObject` | body | `string` | yes | Serialized MobidiQuery payload. |
| `queryName` | body | `string` | yes | Saved query display name. |
