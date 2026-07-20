# Retently Universal API Examples

These examples use the MindCloud API key and Retently connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves a list of customers from Retently.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&attributes%5B%5D.name=Ava%20Chen&attributes%5B%5D.op=string&attributes%5B%5D.value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "attributes[].name": "Ava Chen",
  "attributes[].op": "string",
  "attributes[].value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-customers?${params}`, {
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
      "companyId": "string",
      "companyName": "Ava Chen",
      "createdDate": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "integrationsLists": [
        "string"
      ],
      "isAnonymous": true,
      "isAtRisk": true,
      "isEmailDeliverable": true,
      "isInQueue": true,
      "isInQueueSetAt": "string",
      "jobTitle": "string",
      "lastName": "Chen",
      "lastSurveySent": {},
      "location": {},
      "phoneNumber": "string",
      "properties": [
        {}
      ],
      "source": "string",
      "surveySubscriptionStatus": {},
      "syncId": "string",
      "tags": [
        "string"
      ],
      "updatedDate": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/retently/latest/actions/list-customers).

## Add Feedback Tags

Updates tags on a feedback response in Retently.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/retently/latest/actions/add-feedback-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retently/latest/actions/add-feedback-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Feedback Tags action reference](actions/add-feedback-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/retently/latest/actions/add-feedback-tags).
