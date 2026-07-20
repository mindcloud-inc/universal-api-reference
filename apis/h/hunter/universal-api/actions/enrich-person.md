# Hunter: Enrich Person



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/enrich-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/enrich-person?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/enrich-person?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address to enrich. |
| `linkedinHandle` | string | no |  |
| `clearbitFormat` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeAt": "string",
      "avatar": "string",
      "bio": "string",
      "email": "ava@example.com",
      "emailProvider": "ava@example.com",
      "employment": {},
      "facebook": {},
      "fuzzy": true,
      "geo": {},
      "github": {},
      "googleplus": {},
      "gravatar": {},
      "id": "string",
      "inactiveAt": "string",
      "indexedAt": "string",
      "linkedin": {},
      "location": "string",
      "name": {},
      "phone": "string",
      "site": "string",
      "timeZone": "string",
      "twitter": {},
      "utcOffset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeAt` | string |  |
| `avatar` | string |  |
| `bio` | string |  |
| `email` | string |  |
| `emailProvider` | string |  |
| `employment` | object |  |
| `facebook` | object |  |
| `fuzzy` | boolean |  |
| `geo` | object |  |
| `github` | object |  |
| `googleplus` | object |  |
| `gravatar` | object |  |
| `id` | string |  |
| `inactiveAt` | string |  |
| `indexedAt` | string |  |
| `linkedin` | object |  |
| `location` | string |  |
| `name` | object |  |
| `phone` | string |  |
| `site` | string |  |
| `timeZone` | string |  |
| `twitter` | object |  |
| `utcOffset` | number |  |

## Native endpoint

Through the native Hunter API, this operation is `GET /people/find` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-person.md) for the provider-specific parameters and requirements.

