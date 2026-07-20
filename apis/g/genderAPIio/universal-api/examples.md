# GenderAPI.io Universal API Examples

These examples use the MindCloud API key and GenderAPI.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Remaining Credits

Retrieves remaining API credits from GenderAPI.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-remaining-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-remaining-credits?${params}`, {
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
      "expiresAt": 1,
      "remaining": 1,
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Get Remaining Credits action reference](actions/get-remaining-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/genderAPIio/latest/actions/get-remaining-credits).
