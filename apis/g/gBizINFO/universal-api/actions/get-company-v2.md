# gBizINFO: Get Company (v2)

Retrieves company details from gBizINFO by corporate number.

```
GET https://connect.mindcloud.co/v1/universal/gBizINFO/latest/actions/get-company-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gBizINFO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gBizINFO/latest/actions/get-company-v2?connectionId=$CONNECTION_ID&corporateNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "corporateNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gBizINFO/latest/actions/get-company-v2?${params}`, {
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
| `corporateNumber` | string | yes | The 13-digit Japanese corporate number to look up. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadataFlag` | boolean | no | Include metadata fields in the company response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregatedYear": "string",
      "businessSummary": {},
      "capitalStock": {},
      "closeCause": {},
      "closeDate": {},
      "companySizeFemale": {},
      "companySizeMale": {},
      "companyUrl": {},
      "corporateNumber": "string",
      "dateOfEstablishment": {},
      "employeeNumber": {},
      "foundingYear": {},
      "kana": "string",
      "kind": "string",
      "location": "string",
      "name": "Ava Chen",
      "nameEn": "Ava Chen",
      "postalCode": "string",
      "process": "string",
      "qualificationGrade": {},
      "representativeName": {},
      "status": "string",
      "updateDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregatedYear` | string |  |
| `businessSummary` | object |  |
| `capitalStock` | object |  |
| `closeCause` | object |  |
| `closeDate` | object |  |
| `companySizeFemale` | object |  |
| `companySizeMale` | object |  |
| `companyUrl` | object |  |
| `corporateNumber` | string |  |
| `dateOfEstablishment` | object |  |
| `employeeNumber` | object |  |
| `foundingYear` | object |  |
| `kana` | string |  |
| `kind` | string |  |
| `location` | string |  |
| `name` | string |  |
| `nameEn` | string |  |
| `postalCode` | string |  |
| `process` | string |  |
| `qualificationGrade` | object |  |
| `representativeName` | object |  |
| `status` | string |  |
| `updateDate` | string |  |

## Native endpoint

Through the native gBizINFO API, this operation is `GET /v2/hojin/:corporate_number` (base URL `https://api.info.gbiz.go.jp/hojin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-v2.md) for the provider-specific parameters and requirements.

