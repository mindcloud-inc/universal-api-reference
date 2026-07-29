# Insert Asset Type with Rillion Prime Web Service

Insert an asset type into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AssetType` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, AssetType section. |
| `AssetType.Company` | body | `list<string>` | no | Company to which asset type belongs |
| `AssetType.AssetType` | body | `string` | yes | Asset type |
| `AssetType.Name` | body | `string` | yes | Asset type name |
| `AssetType.Account` | body | `string` | no | Account that asset type is to be used for |
| `AssetType.Group1` | body | `string` | no | Free field of Type 1 |
| `AssetType.Group2` | body | `string` | no | Free field of Type 2 |
| `AssetType.Group3` | body | `string` | no | Free field of Type 3 |
| `AssetType.KeyType` | body | `number` | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `AssetType.ExternalId` | body | `string` | no | — |
| `AssetType.ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
