# Search Catalog Items by Identifier with Amazon Seller

Finds catalog items in Amazon Seller by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `catalog/2022-04-01/items`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Search Catalog Items by Identifier](https://developer-docs.amazon.com/sp-api/reference/searchcatalogitems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifiersType` | query | `list<string>` | yes | The type of product identifier supplied in Identifier. Use SKU for seller SKU lookup or ASIN for Amazon Standard Identification Number lookup. Accepted values: `ASIN`, `EAN`, `GTIN`, `ISBN`, `JAN`, `MINSAN`, `SKU`, `UPC`. |
| `identifiers` | query | `string<string>` | yes | One or more product identifiers to search for. Amazon accepts up to 20 comma-delimited values. Send multiple values as a string separated by `,`. |
| `marketplaceIds` | query | `list<string>` | yes | The Amazon marketplace identifier. Amazon allows at most one marketplace ID for this request. Accepted values: `A13V1IB3VIYZZH`, `A17E79C6D8DWNP`, `A1805IZSGTT6HS`, `A19VAU5U5O7RUS`, `A1AM78C64UM0Y8`, `A1C3SOZRARQ6R3`, `A1F83G8C2ARO7P`, `A1PA6795UKMFR9`, `A1RKKUPIHCS9HS`, `A1VC38T7YXB528`, `A21TJRUUN4KGV`, `A28R8C7NBKEWEA`, `A2EUQ1WTGCTBG2`, `A2NODRKZP88ZB9`, `A2Q3Y263D00KWC`, `A2VIGQ35RCS4UG`, `A33AVAJ2PDY3EV`, `A39IBJ37TRP1C6`, `AE08WJ6YKNBMC`, `AMEN7PMS3EDWL`, `APJ6JRA9NG5V4`, `ARBP9OOSHTCHU`, `ATVPDKIKX0DER`. |
| `sellerId` | query | `string<string>` | no | A selling partner identifier. Required by Amazon when Identifier Type is SKU. |
| `includedData` | query | `list<string>` | no | Datasets to include in the catalog response. Amazon defaults to summaries when omitted. Accepted values: `attributes`, `classifications`, `dimensions`, `identifiers`, `images`, `productTypes`, `relationships`, `salesRanks`, `summaries`, `vendorDetails`. Send multiple values as a string separated by `,`. |
| `locale` | query | `string<string>` | no | Locale for localized summaries. Defaults to the primary locale of the marketplace when omitted. |
