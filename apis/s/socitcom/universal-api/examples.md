# Société.com Universal API Examples

These examples use the MindCloud API key and Société.com connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Client Information

Retrieves client account information from Société.com.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-client-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-client-information?${params}`, {
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
      "compteactif": true,
      "creditmode": "string",
      "creditrestant": "string",
      "derniereversion": "string",
      "nbhit": 1,
      "versioncourante": "string",
      "versions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Client Information action reference](actions/get-client-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/socitcom/latest/actions/get-client-information).
