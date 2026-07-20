# City of Beverly Hills Universal API Examples

These examples use the MindCloud API key and City of Beverly Hills connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Layer

Retrieves feature layer details from City of Beverly Hills.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/get-feature-layer?connectionId=$CONNECTION_ID&layerId=string&serviceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "layerId": "string",
  "serviceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/get-feature-layer?${params}`, {
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
      "currentVersion": 1,
      "fields": [
        [
          {}
        ]
      ],
      "geometryType": "string",
      "id": 1,
      "name": "Ava Chen",
      "objectIdField": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Layer action reference](actions/get-feature-layer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cityOfBeverlyHills/latest/actions/get-feature-layer).
