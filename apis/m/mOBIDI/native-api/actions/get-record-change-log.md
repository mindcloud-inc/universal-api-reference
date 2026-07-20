# Get Record Change Log with MOBIDI

Retrieves a record change log from MOBIDI.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiQueryManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Get Record Change Log](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordID` | body | `string` | yes | MOBIDI record identifier. |
| `UpdateUserNames` | body | `boolean` | no | Whether to resolve user display names in the log. |
