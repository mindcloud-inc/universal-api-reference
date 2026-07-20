# gBizINFO Universal API Examples

These examples use the MindCloud API key and gBizINFO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company (v2)

Retrieves company details from gBizINFO by corporate number.

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

Example response:

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

See the full [Get Company (v2) action reference](actions/get-company-v2.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gBizINFO/latest/actions/get-company-v2).
