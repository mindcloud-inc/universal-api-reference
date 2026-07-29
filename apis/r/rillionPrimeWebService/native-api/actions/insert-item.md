# Insert Item with Rillion Prime Web Service

Insert a purchasing item into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Item` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Item section. |
| `Item.Item` | body | `string` | yes | Item number |
| `Item.ItemFormName` | body | `string` | no | — |
| `Item.Company` | body | `list<string>` | no | Company for the intem |
| `Item.Commodity` | body | `string` | no | Commodity |
| `Item.Supplier` | body | `string` | yes | Supplier |
| `Item.Description` | body | `string` | yes | Description |
| `Item.Note` | body | `string` | no | Detailed description |
| `Item.SupplierItem` | body | `string` | no | Item number from the supplier |
| `Item.Manufacturer` | body | `string` | no | Name of manufacture |
| `Item.ManufacturerItem` | body | `string` | no | Item number from the manufacture |
| `Item.Blocked` | body | `string` | no | Blocked for purchase: 0=No; 1=Yes |
| `Item.ValidFrom` | body | `date` | no | Item availbable from this date |
| `Item.ValidTo` | body | `date` | no | Item availbable to this date |
| `Item.DaysOfDelivery` | body | `number` | no | Delivery term in days (0-366) |
| `Item.ResponsiblePurchaseOrderRole` | body | `string` | no | Responsible purchaser |
| `Item.Account` | body | `string` | no | Default expenditure account |
| `Item.Href` | body | `string` | yes | — |
| `Item.ImageFile` | body | `string` | no | Filename of the image for the item |
| `Item.ImageHref` | body | `string` | no | Url or file reference to image or other document for more details of the item |
| `Item.BestBuy` | body | `string` | no | — |
| `Item.CommodityCode` | body | `string` | no | Commodity code |
| `Item.FileTypeID` | body | `number` | no | File type ID set up in Prime Master |
| `Item.AttachedFile` | body | `string` | no | Filename for import of image to the item |
| `Item.PriceFromDate` | body | `date` | yes | Price valid from this date |
| `Item.Currency` | body | `string` | yes | Currency |
| `Item.Unit` | body | `string` | no | Unit |
| `Item.Price` | body | `number` | yes | Price (gross) |
| `Item.Discount` | body | `number` | yes | Discount in % |
| `Item.Tax` | body | `number` | yes | Tax or additional costs |
| `Item.Group1` | body | `string` | no | Free field of Type 1 |
| `Item.Group2` | body | `string` | no | Free field of Type 2 |
| `Item.Group3` | body | `string` | no | Free field of Type 3 |
| `Item.KeyType` | body | `boolean` | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `Item.UnitNumber` | body | `number` | no | Packaging numbers |
| `Item.MinNumber` | body | `number` | no | Minumum number for ordering |
| `Item.MinExtraNumber` | body | `number` | no | Minumum number of additional order |
| `Item.EcoLabel` | body | `string` | no | Marked as ecolabelled: 0=No; 1=Yes |
| `Item.EcoLabelText` | body | `string` | no | Type of EcoLabelling |
| `Item.DangerousLabel` | body | `string` | no | Marked as dangerous goods: 0=No; 1=Yes |
| `Item.DangerousLabelText` | body | `string` | no | Type of dangerous goods |
| `Item.TagWords` | body | `string` | yes | — |
| `Item.ContractNo` | body | `string` | no | — |
| `Item.ExternalId` | body | `string` | no | — |
| `Item.ExternalSource` | body | `string` | no | — |
| `ItemImage` | body | `object` | no | Optional image payload for the item. |
| `ItemAttachment` | body | `object` | no | Optional attachment payload for the item. |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
