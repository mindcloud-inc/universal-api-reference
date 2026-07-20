# RocketReach Universal API Examples

These examples use the MindCloud API key and RocketReach connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Person Lookup Status

Retrieves person lookup status from RocketReach.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/check-person-lookup-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/check-person-lookup-status?${params}`, {
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
      "birth_year": 1,
      "city": "string",
      "country": "string",
      "country_code": "string",
      "current_employer": "string",
      "current_employer_domain": "string",
      "current_employer_id": 1,
      "current_employer_industry": "string",
      "current_employer_linkedin_url": "https://example.com",
      "current_employer_website": "string",
      "current_personal_email": "ava@example.com",
      "current_title": "string",
      "current_work_email": "ava@example.com",
      "education": [
        {}
      ],
      "emails": [
        {}
      ],
      "id": 1,
      "job_history": [
        {}
      ],
      "linkedin_url": "https://example.com",
      "links": {},
      "location": "string",
      "name": "Ava Chen",
      "phones": [
        {}
      ],
      "profile_list": {},
      "profile_pic": "string",
      "recommended_email": "ava@example.com",
      "recommended_personal_email": "ava@example.com",
      "recommended_professional_email": "ava@example.com",
      "region": "string",
      "return_cached_emails": true,
      "skills": [
        "string"
      ],
      "status": "string",
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Check Person Lookup Status action reference](actions/check-person-lookup-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rocketReach/latest/actions/check-person-lookup-status).

## Bulk Lookup People

Creates a RocketReach bulk people lookup.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/bulk-lookup-people" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/bulk-lookup-people', {
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
  "data": [],
  "meta": {}
}
```

See the full [Bulk Lookup People action reference](actions/bulk-lookup-people.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rocketReach/latest/actions/bulk-lookup-people).
