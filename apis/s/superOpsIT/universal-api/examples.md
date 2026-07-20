# SuperOps IT Universal API Examples

These examples use the MindCloud API key and SuperOps IT connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tickets



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-tickets?${params}`, {
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
      "getTicketList": {
        "listInfo": {
          "page": 1,
          "pageSize": 1,
          "totalCount": 1
        },
        "tickets": [
          {
            "createdTime": "2026-05-07T12:00:00.000Z",
            "displayId": "string",
            "requester": {
              "name": "Ava Chen",
              "userId": "string"
            },
            "site": {
              "id": "string",
              "name": "Ava Chen"
            },
            "status": "string",
            "subject": "string",
            "ticketId": "string",
            "updatedTime": "2026-05-07T12:00:00.000Z"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [List Tickets action reference](actions/list-tickets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/superOpsIT/latest/actions/list-tickets).

## Create Site



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "working24x7": true,
  "timezoneCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "working24x7": true,
    "timezoneCode": "string"
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
      "createSite": {
        "address": {
          "addressId": "string",
          "countryCode": "string"
        },
        "contactNumber": "string",
        "id": "string",
        "name": "Ava Chen",
        "timezoneCode": "string",
        "working24x7": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Site action reference](actions/create-site.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/superOpsIT/latest/actions/create-site).
