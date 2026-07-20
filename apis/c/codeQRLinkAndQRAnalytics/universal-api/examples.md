# CodeQR - Link and QR Analytics Universal API Examples

These examples use the MindCloud API key and CodeQR - Link and QR Analytics connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from CodeQR.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-projects?${params}`, {
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
      "clicks": 1,
      "conversionEnabled": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domains": [
        {}
      ],
      "domainsLimit": 1,
      "id": "string",
      "linksUsage": 1,
      "metadata": {},
      "name": "Ava Chen",
      "plan": "string",
      "qrCodesUsage": 1,
      "scans": 1,
      "slug": "string",
      "tagsLimit": 1,
      "trialEndDate": "2026-05-07T12:00:00.000Z",
      "trialStartDate": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "users": [
        {}
      ],
      "usersLimit": 1,
      "webhookEnabled": true
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/codeQRLinkAndQRAnalytics/latest/actions/list-projects).

## Create Domain

Creates a domain in CodeQR.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/create-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/create-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string"
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
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiredUrl": "https://example.com",
      "id": "string",
      "placeholder": "string",
      "primary": true,
      "slug": "string",
      "target": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "verified": true
    }
  ],
  "meta": {}
}
```

See the full [Create Domain action reference](actions/create-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/codeQRLinkAndQRAnalytics/latest/actions/create-domain).
