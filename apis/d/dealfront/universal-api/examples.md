# Dealfront Universal API Examples

These examples use the MindCloud API key and Dealfront connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves accounts from Dealfront.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-accounts?${params}`, {
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
      "attributes": {
        "name": "Ava Chen",
        "onTrial": true,
        "subscription": "string",
        "subscriptionAddons": [
          "string"
        ],
        "timezone": "string",
        "websiteTrackingStatus": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dealfront/latest/actions/list-accounts).

## Request Feed Export

Creates a new feed export request in Dealfront.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/request-feed-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "customFeedId": "string",
  "startDate": "string",
  "endDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/request-feed-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "customFeedId": "string",
    "startDate": "string",
    "endDate": "string"
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
      "attributes": {
        "createdAt": "string",
        "downloadUrl": "https://example.com",
        "status": "string",
        "statusUrl": "https://example.com"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Request Feed Export action reference](actions/request-feed-export.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dealfront/latest/actions/request-feed-export).
