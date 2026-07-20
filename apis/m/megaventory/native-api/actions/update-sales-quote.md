# Update Sales Quote with Megaventory

Updates a sales quote in Megaventory using a record action.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/SalesQuoteUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Sales Quote](https://api.megaventory.com/v2017a/json/metadata?op=SalesQuoteUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvSalesQuote` | body | `object` | yes | Sales quote payload to insert, update, or delete. |
| `mvRecordAction` | body | `string` | yes | Megaventory record action such as Insert, Update, or Delete. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
| `AutoInsertBundledProductRows` | body | `boolean` | no | Automatically insert bundled product rows when Megaventory supports it. |
