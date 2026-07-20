# Vouchsafe Universal API Examples

These examples use the MindCloud API key and Vouchsafe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Alert Account Detail

Retrieves alert account details from Vouchsafe.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/get-alert-account-detail?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/get-alert-account-detail?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Alert Account Detail action reference](actions/get-alert-account-detail.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vouchsafe/latest/actions/get-alert-account-detail).

## Perform Adverse Media Check

Runs an adverse media check in Vouchsafe.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/perform-adverse-media-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/perform-adverse-media-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Perform Adverse Media Check action reference](actions/perform-adverse-media-check.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vouchsafe/latest/actions/perform-adverse-media-check).
