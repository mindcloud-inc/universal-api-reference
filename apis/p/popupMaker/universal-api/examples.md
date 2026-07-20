# Popup Maker Universal API Examples

These examples use the MindCloud API key and Popup Maker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Connect Account and List Popups

Retrieves connected account details and popups from Popup Maker.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/popupMaker/latest/actions/connect-account-and-list-popups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/popupMaker/latest/actions/connect-account-and-list-popups?${params}`, {
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
      "isAuthenticate": true,
      "popups": {},
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Connect Account and List Popups action reference](actions/connect-account-and-list-popups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/popupMaker/latest/actions/connect-account-and-list-popups).
