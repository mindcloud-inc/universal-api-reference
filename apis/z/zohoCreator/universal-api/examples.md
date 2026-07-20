# Zoho Creator Universal API Examples

These examples use the MindCloud API key and Zoho Creator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Applications

Retrieves accessible applications from Zoho Creator.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-applications?${params}`, {
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
      "applications": [
        {}
      ],
      "code": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Applications action reference](actions/get-applications.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoCreator/latest/actions/get-applications).

## Add Records

Creates new records in a Zoho Creator form.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/add-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountOwnerName": "Ava Chen",
  "appLinkName": "https://example.com",
  "formLinkName": "https://example.com",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/add-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountOwnerName": "Ava Chen",
    "appLinkName": "https://example.com",
    "formLinkName": "https://example.com",
    "data[]": [{}]
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
      "code": 1,
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Records action reference](actions/add-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoCreator/latest/actions/add-records).
