# Set Default Query with MOBIDI

Sets the default query in MOBIDI.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiQueryManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Set Default Query](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queryObject` | body | `string` | yes | Serialized MobidiQuery payload. |
