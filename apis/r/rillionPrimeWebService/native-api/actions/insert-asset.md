# Insert Asset with Rillion Prime Web Service

Insert an asset into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Asset` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Asset section. |
| `Asset.AssetType` | body | `string` | yes | Asset type |
| `Asset.Asset` | body | `string` | yes | Asset |
| `Asset.Company` | body | `list<string>` | yes | Company to which asset belongs |
| `Asset.Name` | body | `string` | yes | Asset name |
| `Asset.Group1` | body | `string` | no | Free field of Type 1 |
| `Asset.Group2` | body | `string` | no | Free field of Type 2 |
| `Asset.Group3` | body | `string` | no | Free field of Type 3 |
| `Asset.ExternalId` | body | `string` | no | — |
| `Asset.ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
