# Grants.gov: Search Opportunities

Finds grant opportunities in Grants.gov by public search filters.

```
GET https://connect.mindcloud.co/v1/universal/grantsgov/latest/actions/search-opportunities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grants.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grantsgov/latest/actions/search-opportunities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grantsgov/latest/actions/search-opportunities?${params}`, {
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
| `keyword` | string | no | Keyword search over public grant opportunity titles and details. |
| `oppNum` | string | no | Funding Opportunity Number to search for. |
| `cfda` | string | no | CFDA or Assistance Listing Number. This key is runtime-verified even though the docs sample still shows aln. |
| `agencies` | string | no | Agency or sub-agency code filter such as HHS or HHS-NIH11. |
| `eligibilities` | string | no | Eligibility code filter such as 01 for county governments. |
| `fundingCategories` | string | no | Funding activity category code such as HL for Health. |
| `oppStatuses` | list | no | One or more opportunity statuses to include. One of: `archived`, `closed`, `forecasted`, `posted`. Accepts multiple values in one string, delimited by `\|`. Default: `forecasted\|posted`. |
| `rows` | number | no | Maximum number of opportunities to return. Default: `10`. |
| `fundingInstruments` | string | no | Funding instrument code such as G for Grant or CA for Cooperative Agreement. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startRecordNum` | number | no | Zero-based record offset for paged search results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agency": "string",
      "agencyCode": "string",
      "cfdaList": [
        "string"
      ],
      "closeDate": "string",
      "docType": "string",
      "id": "string",
      "number": "string",
      "openDate": "string",
      "oppStatus": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agency` | string | Owning agency display name. |
| `agencyCode` | string | Owning agency or sub-agency code. |
| `cfdaList` | array<string> | CFDA / Assistance Listing numbers associated with the opportunity. |
| `closeDate` | string | Opportunity close date as returned by Grants.gov. |
| `docType` | string | Document type such as synopsis or forecast. |
| `id` | string | Grants.gov opportunity identifier returned in search results. |
| `number` | string | Funding Opportunity Number. |
| `openDate` | string | Opportunity open date as returned by Grants.gov. |
| `oppStatus` | string | Opportunity status. |
| `title` | string | Opportunity title. |

## Native endpoint

Through the native Grants.gov API, this operation is `POST /v1/api/search2` (base URL `https://api.grants.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-opportunities.md) for the provider-specific parameters and requirements.

