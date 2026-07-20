# Smarty-streets Universal API Examples

These examples use the MindCloud API key and Smarty-streets connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate US Street Address

Retrieves validated US street addresses from Smarty-streets.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-street-address?connectionId=$CONNECTION_ID&street=1%20Santa%20Claus%20Ln&city=North%20Pole&state=AK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "street": "1 Santa Claus Ln",
  "city": "North Pole",
  "state": "AK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-street-address?${params}`, {
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
      "analysis": {},
      "candidateIndex": 1,
      "components": {},
      "deliveryLine1": "string",
      "inputIndex": 1,
      "lastLine": "string",
      "metadata": {}
    }
  ],
  "meta": {}
}
```

See the full [Validate US Street Address action reference](actions/validate-us-street-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartyStreets/latest/actions/validate-us-street-address).
