# Rebrandly Universal API Examples

These examples use the MindCloud API key and Rebrandly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details

Retrieves details for the current Rebrandly account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-account-details?${params}`, {
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
      "avatarUrl": "https://example.com",
      "clicks": 1,
      "createdAt": "string",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string",
      "registration": {
        "country": "string"
      },
      "scans": {
        "qr": 1
      },
      "subscription": {
        "addonsEligible": true,
        "billing": {
          "cycle": {
            "price": {
              "full": 1,
              "net": 1,
              "vat": 1
            },
            "recurrence": {
              "unit": "string",
              "units": 1
            },
            "resetsAt": "string",
            "trial": {
              "expiresAt": {}
            }
          }
        },
        "category": "string",
        "categoryVariant": "string",
        "createdAt": "string",
        "due": 1,
        "external": {
          "id": {},
          "line": {}
        },
        "id": "string",
        "limits": {
          "apps": {
            "included": 1,
            "used": 1
          },
          "cycle": {
            "clicks": {
              "included": 1,
              "used": 1
            },
            "linksClassic": {
              "included": 1,
              "used": 1
            }
          },
          "domains": {
            "included": 1,
            "used": 1
          },
          "scripts": {
            "included": 1,
            "used": 1
          },
          "tags": {
            "included": 1,
            "used": 1
          },
          "webhooks": {
            "included": 1,
            "used": 1
          },
          "workspaces": {
            "included": 1,
            "used": 1
          }
        },
        "plan": {
          "id": "string",
          "isSlg": true
        },
        "status": {
          "renew": true,
          "suspend": true
        },
        "version": 1
      },
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rebrandly/latest/actions/get-account-details).

## Attach Tag To Link

Attaches a tag to a link in Rebrandly.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/attach-tag-to-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lid": "string",
  "tid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/attach-tag-to-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lid": "string",
    "tid": "string"
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

See the full [Attach Tag To Link action reference](actions/attach-tag-to-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rebrandly/latest/actions/attach-tag-to-link).
