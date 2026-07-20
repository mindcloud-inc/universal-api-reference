# CPSC Recalls Retrieval: Search Recalls

Finds public product recalls in CPSC by search fields.

```
GET https://connect.mindcloud.co/v1/universal/cPSCRecallsRetrieval/latest/actions/search-recalls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CPSC Recalls Retrieval `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cPSCRecallsRetrieval/latest/actions/search-recalls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cPSCRecallsRetrieval/latest/actions/search-recalls?${params}`, {
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
| `recallNumber` | string | no | Find recalls whose recall number matches this value. |
| `recallTitle` | string | no | Find recalls whose title contains this text. |
| `recallDescription` | string | no | Find recalls whose description contains this text. |
| `productName` | string | no | Find recalls by product name text. |
| `recallDateStart` | date | no | Find recalls on or after this recall date. |
| `recallDateEnd` | date | no | Find recalls on or before this recall date. |
| `manufacturer` | string | no | Find recalls by manufacturer or firm name. |
| `hazard` | string | no | Find recalls by hazard text. |
| `remedy` | string | no | Find recalls by remedy text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `consumerContact` | string | no | Find recalls whose consumer contact text matches this value. |
| `lastPublishDateStart` | date | no | Find recalls last published on or after this date. |
| `lastPublishDateEnd` | date | no | Find recalls last published on or before this date. |
| `recallUrl` | string | no | Find recalls whose recall URL matches this value. |
| `productDescription` | string | no | Find recalls by product description text. |
| `productModel` | string | no | Find recalls by product model text. |
| `productType` | string | no | Find recalls by product type text. |
| `recallInconjunctionCountry` | string | no | Find recalls by country involved in a joint recall. |
| `imageUrl` | string | no | Find recalls whose image URL matches this value. |
| `injury` | string | no | Find recalls by injury text. |
| `manufacturerCountry` | string | no | Find recalls by manufacturer country. |
| `upc` | string | no | Find recalls by product UPC. |
| `retailer` | string | no | Find recalls by retailer text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ConsumerContact": "string",
      "Description": "string",
      "Distributors": [
        {}
      ],
      "Hazards": [
        {}
      ],
      "Images": [
        {}
      ],
      "Importers": [
        {}
      ],
      "Inconjunctions": [
        {}
      ],
      "Injuries": [
        {}
      ],
      "LastPublishDate": "2026-05-07T12:00:00.000Z",
      "ManufacturerCountries": [
        {}
      ],
      "Manufacturers": [
        {}
      ],
      "Products": [
        {}
      ],
      "ProductUPCs": [
        {}
      ],
      "RecallDate": "2026-05-07T12:00:00.000Z",
      "RecallID": 1,
      "RecallNumber": "string",
      "Remedies": [
        {}
      ],
      "RemedyOptions": [
        {}
      ],
      "Retailers": [
        {}
      ],
      "SoldAtLabel": "string",
      "Title": "string",
      "URL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ConsumerContact` | string | Consumer contact instructions for the recall. |
| `Description` | string | Recall product description. |
| `Distributors` | array<object> | Distributor records. |
| `Hazards` | array<object> | Hazard records. |
| `Images` | array<object> | Recall image records. |
| `Importers` | array<object> | Importer records. |
| `Inconjunctions` | array<object> | Countries involved in recalls conducted in conjunction with CPSC. |
| `Injuries` | array<object> | Reported injury records. |
| `LastPublishDate` | date | Most recent publication date for the recall record. |
| `ManufacturerCountries` | array<object> | Manufacturer country records. |
| `Manufacturers` | array<object> | Manufacturer or firm records. |
| `Products` | array<object> | Products involved in the recall. |
| `ProductUPCs` | array<object> | Product UPC records. |
| `RecallDate` | date | Date the recall was announced. |
| `RecallID` | number | Numeric CPSC recall identifier. |
| `RecallNumber` | string | CPSC recall number. |
| `Remedies` | array<object> | Remedy records. |
| `RemedyOptions` | array<object> | Structured remedy option records when provided. |
| `Retailers` | array<object> | Retailer records. |
| `SoldAtLabel` | string | Label describing where the product was sold. |
| `Title` | string | Recall title. |
| `URL` | string | CPSC recall detail page URL. |

## Native endpoint

Through the native CPSC Recalls Retrieval API, this operation is `GET /Recall` (base URL `https://www.saferproducts.gov/RestWebServices`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-recalls.md) for the provider-specific parameters and requirements.

