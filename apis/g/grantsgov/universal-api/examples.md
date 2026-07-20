# Grants.gov Universal API Examples

These examples use the MindCloud API key and Grants.gov connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Opportunity

Retrieves grant opportunity details from Grants.gov by opportunity ID.

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

Example response:

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

See the full [Fetch Opportunity action reference](actions/fetch-opportunity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/grantsgov/latest/actions/fetch-opportunity).
