# Happy SMS Universal API Examples

These examples use the MindCloud API key and Happy SMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/get-balance?${params}`, {
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
      "prepaidBalance": 1,
      "smsBalance": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/happySMS/latest/actions/get-balance).

## Create Document



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resource[]": [
    {
      "label": "name",
      "value": "MindCloud Test Document"
    },
    {
      "label": "_tel",
      "value": "+687999999"
    }
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resource[]": [{"label":"name","value":"MindCloud Test Document"},{"label":"_tel","value":"+687999999"}]
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
      "": [
        {
          "key": "string",
          "label": "string",
          "type": "string",
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Document action reference](actions/create-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/happySMS/latest/actions/create-document).
