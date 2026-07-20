# WorkflowMax Universal API Examples

These examples use the MindCloud API key and WorkflowMax connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-current-user?${params}`, {
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
      "Organization": {
        "Name": "Ava Chen"
      },
      "User": {
        "Email": "ava@example.com",
        "Name": "Ava Chen",
        "UUID": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workflowMax/latest/actions/get-current-user).

## Create Client



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-client', {
  method: 'POST',
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
  "data": [
    {
      "addresses": [
        {
          "address": "string",
          "city": "string",
          "country": "string",
          "default": true,
          "postalCode": "string",
          "state": "string",
          "type": "string"
        }
      ],
      "archived": true,
      "billingDetails": {
        "balanceDate": "string",
        "billingClient": {
          "name": "Ava Chen",
          "uuid": "string"
        },
        "businessStructure": {
          "businessStructure": "string",
          "uuid": "string"
        },
        "clientType": {
          "clientType": "string",
          "uuid": "string"
        },
        "customRates": [
          {
            "billableRate": 1,
            "taskUUID": "string"
          }
        ],
        "invoiceDueDate": "string",
        "markup": 1,
        "taxNumbers": [
          {
            "name": "Ava Chen",
            "number": "string"
          }
        ],
        "zeroRatedTaxRate": {
          "rate": 1,
          "taxName": "Ava Chen"
        }
      },
      "clientGroups": [
        {
          "name": "Ava Chen",
          "taxable": true,
          "uuid": "string"
        }
      ],
      "clientManager": {
        "firstName": "Ava",
        "lastName": "Chen",
        "uuid": "string"
      },
      "clientRelationships": [
        {
          "endDate": "string",
          "numberOfShare": 1,
          "relatedClientUUID": "string",
          "startDate": "string",
          "type": "string",
          "uuid": "string"
        }
      ],
      "contactDetails": {
        "email": "ava@example.com",
        "fax": "string",
        "phone": "string",
        "website": "string"
      },
      "contacts": [
        {
          "firstName": "Ava",
          "includeInEmails": true,
          "lastName": "Chen",
          "position": "string",
          "primary": true,
          "salutation": "string",
          "uuid": "string"
        }
      ],
      "createdAt": "string",
      "customFields": [
        {
          "name": "Ava Chen",
          "uuid": "string",
          "value": "string"
        }
      ],
      "exportCode": "string",
      "favorite": true,
      "jobManager": {
        "firstName": "Ava",
        "lastName": "Chen",
        "uuid": "string"
      },
      "name": "Ava Chen",
      "prospect": true,
      "referralSource": "string",
      "updatedAt": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workflowMax/latest/actions/create-client).
