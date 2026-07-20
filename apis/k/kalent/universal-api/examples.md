# Kalent Universal API Examples

These examples use the MindCloud API key and Kalent connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Talents



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kalent/latest/actions/search-talents?connectionId=$CONNECTION_ID&filters%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kalent/latest/actions/search-talents?${params}`, {
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
      "certifications": [
        {}
      ],
      "city": "string",
      "country": "string",
      "currentOrganization": {},
      "educations": [
        {}
      ],
      "experiences": [
        {}
      ],
      "firstname": "Ava",
      "gender": "string",
      "headline": "string",
      "id": "string",
      "interests": [
        "string"
      ],
      "jobTitle": "string",
      "languages": [
        {}
      ],
      "lastname": "Chen",
      "linkedinUrl": "https://example.com",
      "photoUrl": "https://example.com",
      "skills": [
        "string"
      ],
      "state": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Talents action reference](actions/search-talents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kalent/latest/actions/search-talents).
