# Logiwa Legacy WMS Universal API Examples

These examples use the MindCloud API key and Logiwa Legacy WMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Pack Types (SEARCH)

By using these endpoints, the users can obtain all the information that is related to the pack types of the items.

To obtain this information, the users should first reach the Pack Type ID values by using the InventoryItemPackTypeSearch endpoint. After this process, the users will be able to use the InventoryItemPackTypeGet endpoint.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/get-pack-type-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/get-pack-type-info?${params}`, {
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

See the full [List Pack Types (SEARCH) action reference](actions/get-pack-type-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logiwaLegacyWMS/latest/actions/get-pack-type-info).

## Get a Product ID



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/get-a-product-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/get-a-product-id', {
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
  "data": [],
  "meta": {}
}
```

See the full [Get a Product ID action reference](actions/get-a-product-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logiwaLegacyWMS/latest/actions/get-a-product-id).
