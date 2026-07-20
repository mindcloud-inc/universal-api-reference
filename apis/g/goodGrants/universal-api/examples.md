# Good Grants Universal API Examples

These examples use the MindCloud API key and Good Grants connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get account

Retrieves account details from Good Grants.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-account?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "domains": [
        "string"
      ],
      "globalId": "string",
      "languages": [
        {}
      ],
      "name": "Ava Chen",
      "owner": {},
      "product": "string",
      "region": "string",
      "slug": "string",
      "timezone": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goodGrants/latest/actions/get-account).

## Create application

Creates a new application in Good Grants.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/create-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "string",
  "chapter": "string",
  "applicant": "string",
  "season": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/create-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "string",
    "chapter": "string",
    "applicant": "string",
    "season": "string",
    "title": "string"
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
      "applicant": {},
      "application_fields": [
        {}
      ],
      "attachments": [
        {}
      ],
      "auto_score": 1,
      "category": {},
      "chapter": {},
      "comments": "string",
      "contributor_count": 1,
      "contributors": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "custom_deadline": "string",
      "division": {},
      "eligibility_status": "string",
      "files_count": 1,
      "form": {},
      "grant_end_date": "2026-05-07T12:00:00.000Z",
      "grant_status": {},
      "local_id": 1,
      "moderation_status": "string",
      "parent_category": {},
      "payment_status": "string",
      "plagiarism_scan_status": "string",
      "review_status": "string",
      "season": {},
      "slug": "string",
      "status": "string",
      "submitted": "2026-05-07T12:00:00.000Z",
      "tags": "string",
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "user_comments": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create application action reference](actions/create-application.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goodGrants/latest/actions/create-application).
