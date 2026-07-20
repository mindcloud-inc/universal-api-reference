# Sakari SMS Universal API Examples

These examples use the MindCloud API key and Sakari SMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Messages

Retrieves account messages from Sakari SMS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-messages?${params}`, {
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
      "contact": {
        "activecampaign": {
          "id": 1
        },
        "attributes": {},
        "blocked": "2026-05-07T12:00:00.000Z",
        "created": {
          "at": "2026-05-07T12:00:00.000Z",
          "by": {}
        },
        "email": "ava@example.com",
        "error": {
          "code": "string",
          "description": "string"
        },
        "firstName": "Ava",
        "hubspot": {
          "id": 1
        },
        "id": "string",
        "lastName": "Chen",
        "lists": {
          "lists": [
            {
              "doubleOptIn": {},
              "filter": {},
              "id": "string",
              "keyword": "string",
              "name": "Ava Chen",
              "optIn": "2026-05-07T12:00:00.000Z",
              "optInConfirmation": "string",
              "optOut": "2026-05-07T12:00:00.000Z",
              "source": {}
            }
          ]
        },
        "mobile": {
          "country": "string",
          "lineType": "string",
          "number": "string",
          "valid": true,
          "verified": "2026-05-07T12:00:00.000Z"
        },
        "optIn": "2026-05-07T12:00:00.000Z",
        "pipedrive": {
          "id": 1
        },
        "updated": {
          "at": "2026-05-07T12:00:00.000Z",
          "by": {}
        },
        "valid": true
      },
      "conversation": {
        "closed": "2026-05-07T12:00:00.000Z",
        "contact": {
          "activecampaign": {},
          "attributes": {},
          "blocked": "2026-05-07T12:00:00.000Z",
          "created": {},
          "email": "ava@example.com",
          "error": {},
          "firstName": "Ava",
          "hubspot": {},
          "id": "string",
          "lastName": "Chen",
          "lists": [
            {}
          ],
          "mobile": {},
          "optIn": "2026-05-07T12:00:00.000Z",
          "pipedrive": {},
          "updated": {},
          "valid": true
        },
        "id": "string",
        "lastMessage": {
          "contact": {},
          "conversation": {},
          "created": {},
          "error": {},
          "group": {},
          "id": "string",
          "media": [
            {}
          ],
          "message": "string",
          "outgoing": true,
          "phoneNumber": "string",
          "price": 1,
          "read": true,
          "segments": 1,
          "sendAt": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "template": "string",
          "type": "string",
          "updated": {}
        }
      },
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Messages action reference](actions/list-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sakariSMS/latest/actions/list-messages).

## Activate Existing Form

Activates an existing lead form in Sakari SMS.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/activate-existing-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/activate-existing-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string"
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
      "active": "2026-05-07T12:00:00.000Z",
      "conversions": 1,
      "created": {
        "at": "2026-05-07T12:00:00.000Z",
        "by": {
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "name": "Ava Chen",
          "source": "string",
          "subSource": "string"
        }
      },
      "id": "string",
      "impressions": 1,
      "name": "Ava Chen",
      "updated": {
        "at": "2026-05-07T12:00:00.000Z",
        "by": {
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "name": "Ava Chen",
          "source": "string",
          "subSource": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Activate Existing Form action reference](actions/activate-existing-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sakariSMS/latest/actions/activate-existing-form).
