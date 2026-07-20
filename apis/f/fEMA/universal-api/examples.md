# FEMA Universal API Examples

These examples use the MindCloud API key and FEMA connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Disaster Declarations Summaries

Retrieves disaster declaration summaries from FEMA.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-disaster-declarations-summaries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-disaster-declarations-summaries?${params}`, {
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
      "declarationDate": "string",
      "declarationRequestNumber": "string",
      "declarationTitle": "string",
      "declarationType": "string",
      "designatedArea": "string",
      "designatedIncidentTypes": "string",
      "disasterCloseoutDate": {},
      "disasterNumber": 1,
      "femaDeclarationString": "string",
      "fipsCountyCode": "string",
      "fipsStateCode": "string",
      "fyDeclared": 1,
      "hash": "string",
      "hmProgramDeclared": true,
      "iaProgramDeclared": true,
      "id": "string",
      "ihProgramDeclared": true,
      "incidentBeginDate": "string",
      "incidentEndDate": {},
      "incidentId": "string",
      "incidentType": "string",
      "lastIAFilingDate": {},
      "lastRefresh": "string",
      "paProgramDeclared": true,
      "placeCode": "string",
      "region": 1,
      "state": "string",
      "tribalRequest": true
    }
  ],
  "meta": {}
}
```

See the full [List Disaster Declarations Summaries action reference](actions/list-disaster-declarations-summaries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fEMA/latest/actions/list-disaster-declarations-summaries).
