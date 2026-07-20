# Swarm: Refresh Profile

Refreshes a profile in Swarm by LinkedIn username.

```
GET https://connect.mindcloud.co/v1/universal/swarm/latest/actions/refresh-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swarm `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | string |  |
| `certifications` | array<object> |  |
| `current_company_name` | string |  |
| `current_company_website` | string |  |
| `current_location` | string |  |
| `current_title` | string |  |
| `education` | array<object> |  |
| `experience` | array<object> |  |
| `full_name` | string |  |
| `headline` | string |  |
| `id` | string |  |
| `last_refresh_at` | string |  |
| `linkedin_url` | string |  |
| `skills` | array<string> |  |
| `social_media` | array<object> |  |

## Native endpoint

Through the native Swarm API, this operation is `GET /v2/profiles/fetch/refresh` (base URL `https://bee.theswarm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-profile.md) for the provider-specific parameters and requirements.

