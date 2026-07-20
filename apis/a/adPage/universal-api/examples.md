# AdPage Universal API Examples

These examples use the MindCloud API key and AdPage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Agency

Retrieves the current agency from AdPage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adPage/latest/actions/get-agency?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adPage/latest/actions/get-agency?${params}`, {
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
      "cnameDomain": "Ava Chen",
      "complianceAccepted": true,
      "complianceAcceptedDate": {},
      "complianceUrl": {
        "url": "https://example.com"
      },
      "connectedEmail": true,
      "connectedStripe": true,
      "copyright": {},
      "darkColor": "string",
      "darkColorRGB": "string",
      "domain": "string",
      "enabledFunnelBuilder": true,
      "enabledRegister": true,
      "enabledWorkspaces": true,
      "enablePopupBuilder": true,
      "fifthColor": "string",
      "fifthColorRGB": "string",
      "fourthColor": "string",
      "fourthColorRGB": "string",
      "hero": "string",
      "icon": "string",
      "id": "string",
      "logo": "string",
      "name": "Ava Chen",
      "primaryColor": "string",
      "primaryColorRGB": "string",
      "projectDomain": "string",
      "secondaryColor": "string",
      "secondaryColorRGB": "string",
      "tagManagerId": "string",
      "takenSeats": 1,
      "usersNumber": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Agency action reference](actions/get-agency.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/adPage/latest/actions/get-agency).
