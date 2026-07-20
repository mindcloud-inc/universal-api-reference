# Google Ads Universal API Examples

These examples use the MindCloud API key and Google Ads connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accessible Customers



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-accessible-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-accessible-customers?${params}`, {
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
      "id": "string",
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Accessible Customers action reference](actions/list-accessible-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleAds/latest/actions/list-accessible-customers).

## Add Campaign Criterion

Creates a campaign criterion in Google Ads.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/add-campaign-criterion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "operations[].create.campaign": "string",
  "operations[].create.keyword.matchType": "BROAD",
  "operations[].create.keyword.text": "string",
  "operations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/add-campaign-criterion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "operations[].create.campaign": "string",
    "operations[].create.keyword.matchType": "BROAD",
    "operations[].create.keyword.text": "string",
    "operations[]": [{}]
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
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add Campaign Criterion action reference](actions/add-campaign-criterion.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleAds/latest/actions/add-campaign-criterion).
