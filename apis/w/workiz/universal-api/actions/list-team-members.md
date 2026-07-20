# Workiz: List Team Members

Finds all team members in Workiz.

```
GET https://connect.mindcloud.co/v1/universal/workiz/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/list-team-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiz/latest/actions/list-team-members?${params}`, {
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
      "active": true,
      "created": "string",
      "email": "ava@example.com",
      "fieldTech": true,
      "id": "string",
      "name": "Ava Chen",
      "role": "string",
      "serviceAreas": [
        "string"
      ],
      "skills": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | string |  |
| `email` | string |  |
| `fieldTech` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `role` | string |  |
| `serviceAreas` | array |  |
| `skills` | array |  |

## Native endpoint

Through the native Workiz API, this operation is `GET /team/all/` (base URL `https://api.workiz.com/api/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.

