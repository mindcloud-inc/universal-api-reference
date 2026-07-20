# Affinda Universal API Examples

These examples use the MindCloud API key and Affinda connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves all accessible organizations from Affinda.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-organizations?${params}`, {
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
      "avatar": "string",
      "awsMarketplaceLink": "https://example.com",
      "id": 1,
      "identifier": "string",
      "isTrial": true,
      "name": "Ava Chen",
      "resthookSignatureKey": "string",
      "showCustomFieldCreation": true,
      "userRole": "string",
      "usesPortalV3": true,
      "validationToolConfig": {}
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/affinda/latest/actions/list-organizations).
