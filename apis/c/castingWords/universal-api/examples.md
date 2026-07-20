# CastingWords Universal API Examples

These examples use the MindCloud API key and CastingWords connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Prepay Balance

Retrieves prepay balance from CastingWords.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/get-prepay-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/get-prepay-balance?${params}`, {
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
      "balance": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Prepay Balance action reference](actions/get-prepay-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/castingWords/latest/actions/get-prepay-balance).

## Add Extra Editing Upgrade

Updates a CastingWords order to add extra editing.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/add-extra-editing-upgrade" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audiofile_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/add-extra-editing-upgrade', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audiofile_id": "string"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Extra Editing Upgrade action reference](actions/add-extra-editing-upgrade.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/castingWords/latest/actions/add-extra-editing-upgrade).
