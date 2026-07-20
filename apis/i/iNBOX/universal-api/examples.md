# INBOX Universal API Examples

These examples use the MindCloud API key and INBOX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get All Campaigns

Retrieves all campaign records from INBOX.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/get-all-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/get-all-campaigns?${params}`, {
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
      "resultCode": 1,
      "resultMessage": "string",
      "resultObject": {},
      "resultStatus": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get All Campaigns action reference](actions/get-all-campaigns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iNBOX/latest/actions/get-all-campaigns).

## Add Single Contact To List

Adds a contact to an INBOX contact list.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/add-single-contact-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/add-single-contact-to-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "resultCode": 1,
      "resultMessage": "string",
      "resultObject": "string",
      "resultStatus": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Single Contact To List action reference](actions/add-single-contact-to-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iNBOX/latest/actions/add-single-contact-to-list).
