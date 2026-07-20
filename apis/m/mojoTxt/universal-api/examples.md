# MojoTxt Universal API Examples

These examples use the MindCloud API key and MojoTxt connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Export Donations

Retrieves a donation export from MojoTxt.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/export-donations?connectionId=$CONNECTION_ID&limit=25&offset=0&donationIdOrKeyword=string&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "donationIdOrKeyword": "string",
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/export-donations?${params}`, {
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
      "record_count": 1,
      "result": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

See the full [Export Donations action reference](actions/export-donations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mojoTxt/latest/actions/export-donations).

## Create Donation Keyword

Creates a donation keyword in MojoTxt.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/create-donation-keyword" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keyword": "string",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/create-donation-keyword', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keyword": "string",
    "phoneNumber": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "created_id": 1,
      "message": "string",
      "result": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Donation Keyword action reference](actions/create-donation-keyword.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mojoTxt/latest/actions/create-donation-keyword).
