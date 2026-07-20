# Swarm Universal API Examples

These examples use the MindCloud API key and Swarm connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Refresh Profile

Refreshes a profile in Swarm by LinkedIn username.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swarm/latest/actions/refresh-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swarm/latest/actions/refresh-profile?${params}`, {
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
      "about": "string",
      "certifications": [
        {}
      ],
      "current_company_name": "Ava Chen",
      "current_company_website": "string",
      "current_location": "string",
      "current_title": "string",
      "education": [
        {}
      ],
      "experience": [
        {}
      ],
      "full_name": "Ava Chen",
      "headline": "string",
      "id": "string",
      "last_refresh_at": "string",
      "linkedin_url": "https://example.com",
      "skills": [
        "string"
      ],
      "social_media": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Refresh Profile action reference](actions/refresh-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swarm/latest/actions/refresh-profile).
