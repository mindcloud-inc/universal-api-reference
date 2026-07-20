# Grants.gov: Fetch Opportunity

Retrieves grant opportunity details from Grants.gov by opportunity ID.

```
GET https://connect.mindcloud.co/v1/universal/grantsgov/latest/actions/fetch-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grants.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grantsgov/latest/actions/fetch-opportunity?connectionId=$CONNECTION_ID&opportunityId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "opportunityId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grantsgov/latest/actions/fetch-opportunity?${params}`, {
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
| `opportunityId` | number | yes | Numeric Grants.gov opportunity identifier returned by Search Opportunities. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agencyDetails": {},
      "assistCompatible": true,
      "assistURL": "https://example.com",
      "cfdas": [
        {}
      ],
      "closedOpportunityPkgs": [
        {}
      ],
      "docType": "string",
      "draftMode": "string",
      "errorMessages": [
        "string"
      ],
      "flag2006": "string",
      "id": 1,
      "listed": "string",
      "opportunityCategory": {},
      "opportunityNumber": "string",
      "opportunityPkgs": [
        {}
      ],
      "opportunityTitle": "string",
      "originalDueDate": "string",
      "originalDueDateDesc": "string",
      "ost": "string",
      "owningAgencyCode": "string",
      "relatedOpps": [
        {}
      ],
      "revision": 1,
      "synopsis": {},
      "synopsisAttachmentFolders": [
        {}
      ],
      "synopsisDocumentURLs": [
        {}
      ],
      "topAgencyDetails": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agencyDetails` | object | Agency metadata for the opportunity. |
| `assistCompatible` | boolean | Whether the opportunity is ASSIST-compatible. |
| `assistURL` | string | ASSIST URL when available. |
| `cfdas` | array<object> | CFDA / Assistance Listing entries. |
| `closedOpportunityPkgs` | array<object> | Closed application package metadata. |
| `docType` | string | Document type such as synopsis or forecast. |
| `draftMode` | string | Draft mode flag. |
| `errorMessages` | array<string> | Provider error messages, if any. |
| `flag2006` | string | Legacy Grants.gov flag value. |
| `id` | number | Grants.gov opportunity identifier. |
| `listed` | string | Listing flag. |
| `opportunityCategory` | object | Opportunity category metadata. |
| `opportunityNumber` | string | Funding Opportunity Number. |
| `opportunityPkgs` | array<object> | Application package metadata. |
| `opportunityTitle` | string | Opportunity title. |
| `originalDueDate` | string | Original application due date. |
| `originalDueDateDesc` | string | Original application due date description. |
| `ost` | string | Opportunity status token. |
| `owningAgencyCode` | string | Owning agency code. |
| `relatedOpps` | array<object> | Related opportunities. |
| `revision` | number | Opportunity revision number. |
| `synopsis` | object | Detailed synopsis and funding metadata. |
| `synopsisAttachmentFolders` | array<object> | Attachment folder metadata and files. |
| `synopsisDocumentURLs` | array<object> | Supplemental synopsis document URLs. |
| `topAgencyDetails` | object | Top-level agency metadata. |

## Native endpoint

Through the native Grants.gov API, this operation is `POST /v1/api/fetchOpportunity` (base URL `https://api.grants.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-opportunity.md) for the provider-specific parameters and requirements.

