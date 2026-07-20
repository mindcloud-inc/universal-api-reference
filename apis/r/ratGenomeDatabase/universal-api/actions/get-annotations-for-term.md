# Rat Genome Database: Get Annotations For Term



```
GET https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-annotations-for-term
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rat Genome Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-annotations-for-term?connectionId=$CONNECTION_ID&accId=string&speciesTypeKey=1&includeChildren=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accId": "string",
  "speciesTypeKey": "1",
  "includeChildren": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-annotations-for-term?${params}`, {
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
| `accId` | string | yes |  |
| `speciesTypeKey` | number | yes |  |
| `includeChildren` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alteration": "string",
      "alterationLocation": "string",
      "annotatedObjectRgdId": 1,
      "annotationExtension": "string",
      "aspect": "string",
      "associatedWith": "string",
      "createdBy": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "dataSrc": "string",
      "evidence": "string",
      "geneProductFormId": "string",
      "key": 1,
      "lastModifiedBy": 1,
      "lastModifiedDate": "2026-05-07T12:00:00.000Z",
      "molecularEntity": "string",
      "notes": "string",
      "objectName": "Ava Chen",
      "objectSymbol": "string",
      "originalCreatedDate": "2026-05-07T12:00:00.000Z",
      "qualifier": "string",
      "qualifier2": "string",
      "refRgdId": 1,
      "rgdObjectKey": 1,
      "speciesTypeKey": 1,
      "term": "string",
      "termAcc": "string",
      "variantNomenclature": "string",
      "withInfo": "string",
      "xrefSource": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alteration` | string | Alteration description. |
| `alterationLocation` | string | Alteration location. |
| `annotatedObjectRgdId` | number | RGD identifier for the annotated object. |
| `annotationExtension` | string | Annotation extension. |
| `aspect` | string | Ontology aspect. |
| `associatedWith` | string | Associated-with field. |
| `createdBy` | number | Creator identifier. |
| `createdDate` | date | Creation timestamp. |
| `dataSrc` | string | Provider data source. |
| `evidence` | string | Evidence code. |
| `geneProductFormId` | string | Gene product form identifier. |
| `key` | number | Internal annotation key. |
| `lastModifiedBy` | number | Last modifier identifier. |
| `lastModifiedDate` | date | Last modification timestamp. |
| `molecularEntity` | string | Molecular entity value. |
| `notes` | string | Provider notes. |
| `objectName` | string | Annotated object name. |
| `objectSymbol` | string | Annotated object symbol. |
| `originalCreatedDate` | date | Original creation timestamp. |
| `qualifier` | string | Primary qualifier. |
| `qualifier2` | string | Secondary qualifier. |
| `refRgdId` | number | Reference RGD identifier. |
| `rgdObjectKey` | number | Internal object key. |
| `speciesTypeKey` | number | Species type key. |
| `term` | string | Annotation term label. |
| `termAcc` | string | Ontology term accession. |
| `variantNomenclature` | string | Variant nomenclature string. |
| `withInfo` | string | With or from information. |
| `xrefSource` | string | Cross-reference source. |

## Native endpoint

Through the native Rat Genome Database API, this operation is `GET /annotations/:accId/:speciesTypeKey/:includeChildren` (base URL `https://rest.rgd.mcw.edu/rgdws`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-annotations-for-term.md) for the provider-specific parameters and requirements.

