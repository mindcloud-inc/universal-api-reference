# Open Data DC Universal API Examples

These examples use the MindCloud API key and Open Data DC connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Location By Address



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-by-address?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-by-address?${params}`, {
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
      "Message": "string",
      "Result": {
        "addresses": {
          "0": {
            "address": {
              "properties": {
                "FullAddress": "string",
                "Latitude": 1,
                "Longitude": 1,
                "MarId": "string",
                "Ward": "string"
              }
            }
          }
        }
      },
      "Success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Location By Address action reference](actions/get-location-by-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openDataDC/latest/actions/get-location-by-address).

## Create Location Batch



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-location-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address_base64": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-location-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address_base64": "string"
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
      "Message": "string",
      "Result": {
        "addresses": [
          {}
        ]
      },
      "Success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Location Batch action reference](actions/create-location-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openDataDC/latest/actions/create-location-batch).
