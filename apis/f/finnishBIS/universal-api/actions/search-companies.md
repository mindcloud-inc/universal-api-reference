# Finnish BIS: Search Companies

Finds companies in Finnish BIS.

```
GET https://connect.mindcloud.co/v1/universal/finnishBIS/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish BIS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishBIS/latest/actions/search-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishBIS/latest/actions/search-companies?${params}`, {
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
| `name` | string | no | Company name. Searches current, previous, parallel, and auxiliary company names. |
| `businessId` | string | no | Finnish Business ID, for example 0116297-6. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `location` | string | no | Town or city. |
| `companyForm` | list<string> | no | Company form code from the PRH YRMU code list. One of: `AOY`, `ASH`, `ASY`, `AY`, `AYH`, `ETS`, `ETY`, `HY`, `KOY`, `KVJ`, `KVY`, `KY`, `OK`, `OP`, `OY`, `OYJ`, `SCE`, `SCP`, `SE`, `SL`, `SP`, `SÄÄ`, `TYH`, `VALTLL`, `VOJ`, `VOY`, `VY`. |
| `mainBusinessLine` | string | no | Statistics Finland TOL 2008 main business line code or text. |
| `registrationDateStart` | date | no | Company registration date range start in yyyy-mm-dd format. |
| `registrationDateEnd` | date | no | Company registration date range end in yyyy-mm-dd format. |
| `postCode` | string | no | Postal code of street or postal address. |
| `businessIdRegistrationStart` | date | no | Business ID grant date range start in yyyy-mm-dd format. |
| `businessIdRegistrationEnd` | date | no | Business ID grant date range end in yyyy-mm-dd format. |
| `page` | number | no | Results page number. If omitted or out of range, PRH returns the first page. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "businessId": {},
      "companyForms": [
        {}
      ],
      "companySituations": [
        {}
      ],
      "euId": {},
      "lastModified": "2026-05-07T12:00:00.000Z",
      "mainBusinessLine": {},
      "names": [
        {}
      ],
      "registeredEntries": [
        {}
      ],
      "registrationDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "tradeRegisterStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> | Company address records. |
| `businessId` | object | Finnish Business ID object, including the displayed value. |
| `companyForms` | array<object> | Company-form classifications. |
| `companySituations` | array<object> | Company situation/status classifications. |
| `euId` | object | EU identifier object when available. |
| `lastModified` | date | Last modification timestamp for this result. |
| `mainBusinessLine` | object | Primary business-line classification for the company. |
| `names` | array<object> | Company names returned by the BIS search result. |
| `registeredEntries` | array<object> | Registry entries associated with the company. |
| `registrationDate` | date | Company registration date. |
| `status` | string | Overall company status. |
| `tradeRegisterStatus` | string | Trade-register status. |

## Native endpoint

Through the native Finnish BIS API, this operation is `GET /companies` (base URL `https://avoindata.prh.fi/opendata-ytj-api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

