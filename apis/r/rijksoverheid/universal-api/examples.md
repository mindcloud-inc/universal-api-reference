# Rijksoverheid Universal API Examples

These examples use the MindCloud API key and Rijksoverheid connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get School Holidays By School Year

Retrieves school holidays for a school year from Rijksoverheid.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksoverheid/latest/actions/get-school-holidays-by-school-year?connectionId=$CONNECTION_ID&schoolYear=2029-2030" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schoolYear": "2029-2030"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rijksoverheid/latest/actions/get-school-holidays-by-school-year?${params}`, {
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
      "authorities": [
        "string"
      ],
      "canonical": "string",
      "content": [
        {}
      ],
      "creators": [
        "string"
      ],
      "id": "string",
      "language": "string",
      "lastmodified": "2026-05-07T12:00:00.000Z",
      "license": "string",
      "location": "string",
      "notice": "string",
      "rightsholders": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get School Holidays By School Year action reference](actions/get-school-holidays-by-school-year.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rijksoverheid/latest/actions/get-school-holidays-by-school-year).
