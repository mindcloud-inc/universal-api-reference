# Get Next Or Previous Record with MOBIDI

Retrieves the next or previous record in MOBIDI.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiQueryManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Get Next Or Previous Record](https://servis2.dece.com.tr/mobidiquerymanagerhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currentRecordId` | body | `string` | yes | Current MOBIDI record identifier. |
| `IsMap` | body | `boolean` | no | Whether to use map navigation mode. |
