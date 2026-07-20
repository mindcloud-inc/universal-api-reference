# IPInfo Universal API Examples

These examples use the MindCloud API key and IPInfo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Lite My IP Details



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/get-lite-my-ip-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/get-lite-my-ip-details?${params}`, {
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
      "asDomain": "string",
      "asn": "string",
      "asName": "Ava Chen",
      "continent": "string",
      "continentCode": "string",
      "country": "string",
      "countryCode": "string",
      "ip": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Lite My IP Details action reference](actions/get-lite-my-ip-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iPInfo/latest/actions/get-lite-my-ip-details).

## Create IP Map



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/create-ip-map" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ipAddresses": "8.8.8.8\n1.1.1.1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/create-ip-map', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ipAddresses": "8.8.8.8\n1.1.1.1"
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
      "reportUrl": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create IP Map action reference](actions/create-ip-map.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iPInfo/latest/actions/create-ip-map).
