# RICOH360 Tours Universal API Examples

These examples use the MindCloud API key and RICOH360 Tours connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Team By API Key



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/get-team-by-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/get-team-by-api-key?${params}`, {
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
      "data": {
        "Type": {
          "fields": [
            {
              "name": "Ava Chen",
              "type": {
                "kind": "string",
                "name": "Ava Chen",
                "ofType": {}
              }
            }
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Team By API Key action reference](actions/get-team-by-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rICOH360Tours/latest/actions/get-team-by-api-key).

## Apply Image Blur



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/apply-image-blur" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/apply-image-blur', {
  method: 'PUT',
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

See the full [Apply Image Blur action reference](actions/apply-image-blur.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rICOH360Tours/latest/actions/apply-image-blur).
