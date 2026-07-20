# Bedrijfsdata.nl: Lookup Property Details



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-property-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-property-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-property-details?${params}`, {
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
| `addressid` | string | no | Bedrijfsdata address ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "monthlyCredits": 1,
      "product": "string",
      "property": {
        "address": "string",
        "addressid": "string",
        "adrestype": "string",
        "bouwjaar": "string",
        "city": "string",
        "district": "string",
        "energielabel": {},
        "freeformaddress": "string",
        "gebruiksdoel": "string",
        "grondoppervlakte": "string",
        "huisletter": "string",
        "huisnummer": "string",
        "lat": "string",
        "lkpId": "string",
        "lon": "string",
        "municipality": "string",
        "neighbourhood": "string",
        "numId": "string",
        "oppervlakte": "string",
        "oprId": "string",
        "perceel": [
          {
            "kadastraalPerceelNummer": "string",
            "kadastraleGemeenteCode": "string",
            "kadastraleSectie": "string"
          }
        ],
        "pndId": "string",
        "postcode": "string",
        "province": "string",
        "provinceCode": "string",
        "street": "string",
        "streetShort": "string",
        "toevoeging": "string",
        "typeadresseerbaarobject": "string",
        "vboId": "string",
        "waterschapsnaam": "string",
        "woz": "string",
        "wozId": "string",
        "wozPanddata": [
          {
            "bagpandidentificatie": 1
          }
        ],
        "wozWaarden": [
          {
            "peildatum": "string",
            "vastgesteldeWaarde": 1
          }
        ],
        "wozYear": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `property.address` | string |  |
| `property.addressid` | string |  |
| `property.adrestype` | string |  |
| `property.bouwjaar` | string |  |
| `property.city` | string |  |
| `property.district` | string |  |
| `property.energielabel` | object |  |
| `property.freeformaddress` | string |  |
| `property.gebruiksdoel` | string |  |
| `property.grondoppervlakte` | string |  |
| `property.huisletter` | string |  |
| `property.huisnummer` | string |  |
| `property.lat` | string |  |
| `property.lkpId` | string |  |
| `property.lon` | string |  |
| `property.municipality` | string |  |
| `property.neighbourhood` | string |  |
| `property.numId` | string |  |
| `property.oppervlakte` | string |  |
| `property.oprId` | string |  |
| `property.perceel[].kadastraalPerceelNummer` | string |  |
| `property.perceel[].kadastraleGemeenteCode` | string |  |
| `property.perceel[].kadastraleSectie` | string |  |
| `property.pndId` | string |  |
| `property.postcode` | string |  |
| `property.province` | string |  |
| `property.provinceCode` | string |  |
| `property.street` | string |  |
| `property.streetShort` | string |  |
| `property.toevoeging` | string |  |
| `property.typeadresseerbaarobject` | string |  |
| `property.vboId` | string |  |
| `property.waterschapsnaam` | string |  |
| `property.woz` | string |  |
| `property.wozId` | string |  |
| `property.wozPanddata[].bagpandidentificatie` | number |  |
| `property.wozWaarden[].peildatum` | string |  |
| `property.wozWaarden[].vastgesteldeWaarde` | number |  |
| `property.wozYear` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /property` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-property-details.md) for the provider-specific parameters and requirements.

