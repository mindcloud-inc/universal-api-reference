# Finnish BIS Universal API Examples

These examples use the MindCloud API key and Finnish BIS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Companies

Finds companies in Finnish BIS.

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

Example response:

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

See the full [Search Companies action reference](actions/search-companies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finnishBIS/latest/actions/search-companies).
