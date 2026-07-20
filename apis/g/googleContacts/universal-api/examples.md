# Google Contacts Universal API Examples

These examples use the MindCloud API key and Google Contacts connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Batch Get Contact Groups

Retrieves multiple contact groups from Google Contacts.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-get-contact-groups?connectionId=$CONNECTION_ID&resourceNames=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceNames": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-get-contact-groups?${params}`, {
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
      "responses": [
        {
          "contactGroup": {
            "etag": "string",
            "formattedName": "Ava Chen",
            "groupType": "string",
            "memberCount": 1,
            "memberResourceNames": [
              "Ava Chen"
            ],
            "metadata": {
              "updateTime": "2026-05-07T12:00:00.000Z"
            },
            "name": "Ava Chen",
            "resourceName": "Ava Chen"
          },
          "requestedResourceName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Batch Get Contact Groups action reference](actions/batch-get-contact-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleContacts/latest/actions/batch-get-contact-groups).

## Batch Create Contacts

Creates multiple new contacts in Google Contacts.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-create-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ],
  "readMask": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-create-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}],
    "readMask": "string"
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
      "createdPeople": [
        {
          "httpStatusCode": 1,
          "person": {
            "emailAddresses": [
              {
                "metadata": {
                  "primary": true,
                  "source": {
                    "id": "ava@example.com",
                    "type": "ava@example.com"
                  }
                },
                "value": "ava@example.com"
              }
            ],
            "etag": "string",
            "metadata": {
              "objectType": "string",
              "sources": [
                {
                  "etag": "string",
                  "id": "string",
                  "type": "string",
                  "updateTime": "2026-05-07T12:00:00.000Z"
                }
              ]
            },
            "names": [
              {
                "displayName": "Ava Chen",
                "displayNameLastFirst": "Ava Chen",
                "familyName": "Ava Chen",
                "givenName": "Ava Chen",
                "metadata": {
                  "primary": true,
                  "source": {
                    "id": "Ava Chen",
                    "type": "Ava Chen"
                  },
                  "sourcePrimary": true
                },
                "unstructuredName": "Ava Chen"
              }
            ],
            "resourceName": "Ava Chen"
          },
          "requestedResourceName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Batch Create Contacts action reference](actions/batch-create-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleContacts/latest/actions/batch-create-contacts).
