# Veteran Confirmation Universal API Examples

These examples use the MindCloud API key and Veteran Confirmation connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Confirm Veteran Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteranConfirmation/latest/actions/confirm-veteran-status?connectionId=$CONNECTION_ID&firstName=Alfredo&lastName=Armstrong&birthDate=1993-06-08&streetAddressLine1=17020%20Tortoise%20St&city=Round%20Rock&state=TX&zipCode=78664&country=USA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstName": "Alfredo",
  "lastName": "Armstrong",
  "birthDate": "1993-06-08",
  "streetAddressLine1": "17020 Tortoise St",
  "city": "Round Rock",
  "state": "TX",
  "zipCode": "78664",
  "country": "USA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veteranConfirmation/latest/actions/confirm-veteran-status?${params}`, {
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
      "id": {},
      "notConfirmedReason": "string",
      "veteranStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Confirm Veteran Status action reference](actions/confirm-veteran-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/veteranConfirmation/latest/actions/confirm-veteran-status).
