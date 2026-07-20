# Metance Universal API Examples

These examples use the MindCloud API key and Metance connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Company

Retrieves the current company from Metance.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-current-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-current-company?${params}`, {
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
      "countryCode": "string",
      "id": 1,
      "logoPath": "string",
      "membersCount": 1,
      "name": "Ava Chen",
      "status": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Company action reference](actions/get-current-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/metance/latest/actions/get-current-company).
