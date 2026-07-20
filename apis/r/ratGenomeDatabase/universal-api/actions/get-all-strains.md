# Rat Genome Database: Get All Strains



```
GET https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-all-strains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rat Genome Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-all-strains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-all-strains?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "backgroundStrainRgdId": 1,
      "chrAltered": "string",
      "color": "string",
      "description": "string",
      "genetics": "string",
      "geneticStatus": "string",
      "imageUrl": "https://example.com",
      "inbredGen": "string",
      "key": 1,
      "lastStatus": "string",
      "lastStatusObject": {},
      "modificationMethod": "string",
      "name": "Ava Chen",
      "notes": "string",
      "origin": "string",
      "origination": "string",
      "researchUse": "string",
      "rgdId": 1,
      "source": "string",
      "speciesTypeKey": 1,
      "statusLog": [
        {}
      ],
      "strain": "string",
      "strainTypeName": "Ava Chen",
      "substrain": "string",
      "symbol": "string",
      "taglessStrainSymbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backgroundStrainRgdId` | number | Background strain RGD identifier when available. |
| `chrAltered` | string | Altered chromosome label. |
| `color` | string | Strain color. |
| `description` | string | Long-form description. |
| `genetics` | string | Genetics summary. |
| `geneticStatus` | string | Genetic status. |
| `imageUrl` | string | Image URL when available. |
| `inbredGen` | string | Inbred generation. |
| `key` | number | Internal strain key. |
| `lastStatus` | string | Latest status label. |
| `lastStatusObject` | object | Most recent status object. |
| `modificationMethod` | string | Modification method. |
| `name` | string | Strain name. |
| `notes` | string | Provider notes. |
| `origin` | string | Origin information. |
| `origination` | string | Origination details. |
| `researchUse` | string | Research use notes. |
| `rgdId` | number | RGD identifier for the strain. |
| `source` | string | Provider source. |
| `speciesTypeKey` | number | Species type key. |
| `statusLog` | array<object> | Status history entries. |
| `strain` | string | Strain label. |
| `strainTypeName` | string | Strain type name. |
| `substrain` | string | Substrain label. |
| `symbol` | string | Strain symbol. |
| `taglessStrainSymbol` | string | Tagless strain symbol. |

## Native endpoint

Through the native Rat Genome Database API, this operation is `GET /strains/all` (base URL `https://rest.rgd.mcw.edu/rgdws`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-strains.md) for the provider-specific parameters and requirements.

