# Rithum for Brands Universal API Examples

These examples use the MindCloud API key and Rithum for Brands connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Profiles



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-profiles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-profiles?${params}`, {
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
      "accountName": "Ava Chen",
      "companyName": "Ava Chen",
      "currencyCode": "string",
      "defaultDistributionCenterID": 1,
      "id": 1,
      "timeZoneDescription": "string",
      "timeZoneRegion": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Profiles action reference](actions/list-profiles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rithumForBrands/latest/actions/list-profiles).

## Create a Product



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/create-a-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileID": 1,
  "sku": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/create-a-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileID": 1,
    "sku": "string",
    "title": "string"
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

See the full [Create a Product action reference](actions/create-a-product.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rithumForBrands/latest/actions/create-a-product).
