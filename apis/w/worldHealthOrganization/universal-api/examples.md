# World Health Organization Universal API Examples

These examples use the MindCloud API key and World Health Organization connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Dimension

Retrieves a dimension from the World Health Organization.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/get-dimension?connectionId=$CONNECTION_ID&dimensionCode=REGION" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dimensionCode": "REGION"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/get-dimension?${params}`, {
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
      "Code": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Dimension action reference](actions/get-dimension.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/worldHealthOrganization/latest/actions/get-dimension).
