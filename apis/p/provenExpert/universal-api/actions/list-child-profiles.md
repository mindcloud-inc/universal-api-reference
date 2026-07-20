# ProvenExpert: List Child Profiles

Lists child profiles in ProvenExpert.

```
GET https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-child-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-child-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-child-profiles?${params}`, {
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
      "company": "string",
      "created": 1,
      "email": "ava@example.com",
      "firstname": "Ava",
      "lastname": "Chen",
      "profileUrl": "https://example.com",
      "public": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | Company name when the child profile is a company profile. |
| `created` | number | Unix timestamp for when the child profile was created. |
| `email` | string | Email address for the child profile. |
| `firstname` | string | First name when the child profile is a personal profile. |
| `lastname` | string | Last name when the child profile is a personal profile. |
| `profileUrl` | string | Public URL for the child profile. |
| `public` | number | Whether the child profile is public. |

## Native endpoint

Through the native ProvenExpert API, this operation is `GET /profile/children` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-child-profiles.md) for the provider-specific parameters and requirements.

