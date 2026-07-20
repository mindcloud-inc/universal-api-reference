# CATS Universal API Examples

These examples use the MindCloud API key and CATS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Site

Retrieves site details from the CATS account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-site?${params}`, {
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
      "defaultCompanyId": 1,
      "Embedded": {
        "defaultCompany": {
          "address": {
            "city": {},
            "postalCode": {},
            "state": {},
            "street": {}
          },
          "billingContactId": {},
          "countryCode": {},
          "dateCreated": "string",
          "dateModified": "string",
          "enteredById": 1,
          "id": 1,
          "isHot": true,
          "keyTechnologies": {},
          "Links": {
            "self": {
              "href": "https://example.com"
            }
          },
          "name": "Ava Chen",
          "notes": "string",
          "ownerId": 1,
          "phones": {
            "fax": {},
            "primary": {},
            "secondary": {}
          },
          "statusId": 1,
          "website": {}
        },
        "users": [
          {
            "firstName": "Ava",
            "id": 1,
            "lastName": "Chen",
            "Links": {
              "self": {
                "href": "https://example.com"
              }
            },
            "title": "string",
            "username": "Ava Chen"
          }
        ]
      },
      "id": 1,
      "Links": {
        "defaultCompany": {
          "href": "https://example.com"
        },
        "self": {
          "href": "https://example.com"
        },
        "users": {
          "href": "https://example.com"
        }
      },
      "mode": "string",
      "subdomain": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Site action reference](actions/get-site.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cATS/latest/actions/get-site).

## Change Job Status

Updates the status of a job in CATS.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/change-job-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "16789175",
  "statusId": "6448583"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cATS/latest/actions/change-job-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "16789175",
    "statusId": "6448583"
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

See the full [Change Job Status action reference](actions/change-job-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cATS/latest/actions/change-job-status).
