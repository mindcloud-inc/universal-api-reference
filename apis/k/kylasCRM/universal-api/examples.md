# Kylas CRM Universal API Examples

These examples use the MindCloud API key and Kylas CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Lead Duplicates



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/check-lead-duplicates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/check-lead-duplicates?${params}`, {
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
      "hasDuplicate": true,
      "message": "string",
      "metaData": {},
      "records": {}
    }
  ],
  "meta": {}
}
```

See the full [Check Lead Duplicates action reference](actions/check-lead-duplicates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kylasCRM/latest/actions/check-lead-duplicates).

## Add Currencies



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/add-currencies" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/add-currencies', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "active": true,
      "baseCurrency": true,
      "createdAt": "string",
      "currencyValueId": 1,
      "displayName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "tenantId": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Currencies action reference](actions/add-currencies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kylasCRM/latest/actions/add-currencies).
