# Twenty Universal API Examples

These examples use the MindCloud API key and Twenty connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List People



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-people?${params}`, {
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
      "avatarFile": "string",
      "avatarUrl": "https://example.com",
      "city": "string",
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "name": "Ava Chen",
        "source": "string"
      },
      "deletedAt": "string",
      "emails": {
        "additionalEmails": [
          "ava@example.com"
        ],
        "primaryEmail": "ava@example.com"
      },
      "id": "string",
      "jobTitle": "string",
      "linkedinLink": {
        "primaryLinkLabel": "https://example.com",
        "primaryLinkUrl": "https://example.com",
        "secondaryLinks": [
          "https://example.com"
        ]
      },
      "name": {
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "phones": {
        "additionalPhones": [
          "string"
        ],
        "primaryPhoneCallingCode": "string",
        "primaryPhoneCountryCode": "string",
        "primaryPhoneNumber": "string"
      },
      "position": 1,
      "searchVector": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": {
        "name": "Ava Chen",
        "source": "string"
      },
      "xLink": {
        "primaryLinkLabel": "https://example.com",
        "primaryLinkUrl": "https://example.com",
        "secondaryLinks": [
          "https://example.com"
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [List People action reference](actions/list-people.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/twenty/latest/actions/list-people).

## Create Company



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twenty/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idealCustomerProfile": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twenty/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idealCustomerProfile": true
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
      "accountOwnerId": "string",
      "address": {
        "addressCity": "string",
        "addressCountry": "string",
        "addressPostcode": "string",
        "addressState": "string",
        "addressStreet1": "string",
        "addressStreet2": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "name": "Ava Chen",
        "source": "string"
      },
      "deletedAt": "string",
      "domainName": {
        "primaryLinkLabel": "https://example.com",
        "primaryLinkUrl": "https://example.com",
        "secondaryLinks": [
          "https://example.com"
        ]
      },
      "employees": 1,
      "id": "string",
      "idealCustomerProfile": true,
      "linkedinLink": {
        "primaryLinkLabel": "https://example.com",
        "primaryLinkUrl": "https://example.com",
        "secondaryLinks": [
          "https://example.com"
        ]
      },
      "name": "Ava Chen",
      "position": 1,
      "searchVector": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": {
        "name": "Ava Chen",
        "source": "string"
      },
      "xLink": {
        "primaryLinkLabel": "https://example.com",
        "primaryLinkUrl": "https://example.com",
        "secondaryLinks": [
          "https://example.com"
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/twenty/latest/actions/create-company).
