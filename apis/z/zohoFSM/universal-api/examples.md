# Zoho FSM Universal API Examples

These examples use the MindCloud API key and Zoho FSM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Requests

Retrieves requests from Zoho FSM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-requests?${params}`, {
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
      "billingAddress": {
        "billingCity": "string",
        "billingCountry": "string",
        "billingState": "string",
        "billingStreet1": "string",
        "billingZipCode": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "cancelledOrTerminatedTime": "2026-05-07T12:00:00.000Z",
      "closedTime": "2026-05-07T12:00:00.000Z",
      "company": {
        "id": "string",
        "name": "Ava Chen"
      },
      "completedTime": "2026-05-07T12:00:00.000Z",
      "contact": {
        "id": "string",
        "name": "Ava Chen"
      },
      "createdBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "estimateRequired": true,
      "exchangeRate": 1,
      "id": "string",
      "modifiedBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owner": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "phone": "string",
      "serviceAddress": {
        "id": "string",
        "name": "Ava Chen",
        "serviceCity": "string",
        "serviceCountry": "string",
        "serviceState": "string",
        "serviceStreet1": "string",
        "serviceZipCode": "string"
      },
      "status": "string",
      "summary": "string",
      "territory": {
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Requests action reference](actions/list-requests.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoFSM/latest/actions/list-requests).

## Create Company

Creates a new company in Zoho FSM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[0].Company_Name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[0].Company_Name": "Ava Chen"
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
      "companies": [
        {
          "createdBy": {
            "id": "string",
            "name": "Ava Chen"
          },
          "createdTime": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "modifiedBy": {
            "id": "string",
            "name": "Ava Chen"
          },
          "modifiedTime": "2026-05-07T12:00:00.000Z",
          "tabName": "Ava Chen",
          "uid": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoFSM/latest/actions/create-company).
