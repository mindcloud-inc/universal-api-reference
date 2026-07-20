# Amazon Seller: Search Catalog Items by Identifier

Finds catalog items in Amazon Seller by identifier.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/search-catalog-items-by-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/search-catalog-items-by-identifier?connectionId=$CONNECTION_ID&identifiersType=SKU&identifiers=MY-SKU-001&marketplaceIds=ATVPDKIKX0DER" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifiersType": "SKU",
  "identifiers": "MY-SKU-001",
  "marketplaceIds": "ATVPDKIKX0DER"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/search-catalog-items-by-identifier?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifiersType` | list<string> | yes | The type of product identifier supplied in Identifier. Use SKU for seller SKU lookup or ASIN for Amazon Standard Identification Number lookup. One of: `ASIN`, `EAN`, `GTIN`, `ISBN`, `JAN`, `MINSAN`, `SKU`, `UPC`. Example: `SKU`. |
| `identifiers` | string<string> | yes | One or more product identifiers to search for. Amazon accepts up to 20 comma-delimited values. Accepts multiple values in one string, delimited by `,`. Example: `MY-SKU-001`. |
| `marketplaceIds` | list<string> | yes | The Amazon marketplace identifier. Amazon allows at most one marketplace ID for this request. One of: `A13V1IB3VIYZZH`, `A17E79C6D8DWNP`, `A1805IZSGTT6HS`, `A19VAU5U5O7RUS`, `A1AM78C64UM0Y8`, `A1C3SOZRARQ6R3`, `A1F83G8C2ARO7P`, `A1PA6795UKMFR9`, `A1RKKUPIHCS9HS`, `A1VC38T7YXB528`, `A21TJRUUN4KGV`, `A28R8C7NBKEWEA`, `A2EUQ1WTGCTBG2`, `A2NODRKZP88ZB9`, `A2Q3Y263D00KWC`, `A2VIGQ35RCS4UG`, `A33AVAJ2PDY3EV`, `A39IBJ37TRP1C6`, `AE08WJ6YKNBMC`, `AMEN7PMS3EDWL`, `APJ6JRA9NG5V4`, `ARBP9OOSHTCHU`, `ATVPDKIKX0DER`. Example: `ATVPDKIKX0DER`. |
| `sellerId` | string<string> | no | A selling partner identifier. Required by Amazon when Identifier Type is SKU. Example: `A1EXAMPLESELLER`. |
| `includedData` | list<string> | no | Datasets to include in the catalog response. Amazon defaults to summaries when omitted. One of: `attributes`, `classifications`, `dimensions`, `identifiers`, `images`, `productTypes`, `relationships`, `salesRanks`, `summaries`, `vendorDetails`. Accepts multiple values in one string, delimited by `,`. Example: `summaries`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locale` | string<string> | no | Locale for localized summaries. Defaults to the primary locale of the marketplace when omitted. Example: `en_US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "asin": "string",
          "identifiers": [
            {
              "identifiers": [
                {
                  "identifier": "string",
                  "identifierType": "string"
                }
              ],
              "marketplaceId": "string"
            }
          ],
          "images": [
            {
              "images": [
                {
                  "height": 1,
                  "link": "https://example.com",
                  "variant": "string",
                  "width": 1
                }
              ],
              "marketplaceId": "string"
            }
          ],
          "summaries": [
            {
              "brand": "string",
              "color": "string",
              "itemClassification": "string",
              "itemName": "Ava Chen",
              "manufacturer": "string",
              "marketplaceId": "string",
              "modelNumber": "string",
              "partNumber": "string",
              "size": "string",
              "style": "string",
              "websiteDisplayGroupName": "Ava Chen"
            }
          ]
        }
      ],
      "numberOfResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Catalog items returned by Amazon. |
| `items[].asin` | string | Amazon Standard Identification Number. |
| `items[].identifiers` | array<object> | Identifiers associated with the catalog item. |
| `items[].identifiers[].identifiers` | array<object> | Identifier values for the catalog item. |
| `items[].identifiers[].identifiers[].identifier` | string | Identifier value. |
| `items[].identifiers[].identifiers[].identifierType` | string | Identifier type, such as SKU, ASIN, EAN, GTIN, ISBN, or UPC. |
| `items[].identifiers[].marketplaceId` | string | Marketplace for the identifier set. |
| `items[].images` | array<object> | Image groups for the catalog item. |
| `items[].images[].images` | array<object> | Images for the catalog item. |
| `items[].images[].images[].height` | number | Image height in pixels. |
| `items[].images[].images[].link` | string | Image URL. |
| `items[].images[].images[].variant` | string | Image variant. |
| `items[].images[].images[].width` | number | Image width in pixels. |
| `items[].images[].marketplaceId` | string | Marketplace for the image group. |
| `items[].summaries` | array<object> | Localized item summaries. |
| `items[].summaries[].brand` | string | Catalog item brand. |
| `items[].summaries[].color` | string | Color when available. |
| `items[].summaries[].itemClassification` | string | Amazon item classification. |
| `items[].summaries[].itemName` | string | Catalog item title. |
| `items[].summaries[].manufacturer` | string | Catalog item manufacturer. |
| `items[].summaries[].marketplaceId` | string | Marketplace for the summary. |
| `items[].summaries[].modelNumber` | string | Model number when available. |
| `items[].summaries[].partNumber` | string | Part number when available. |
| `items[].summaries[].size` | string | Size when available. |
| `items[].summaries[].style` | string | Style when available. |
| `items[].summaries[].websiteDisplayGroupName` | string | Amazon website display group name. |
| `numberOfResults` | number | Number of catalog items returned by Amazon for the identifier search. |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET catalog/2022-04-01/items` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-catalog-items-by-identifier.md) for the provider-specific parameters and requirements.

