# Tomba: LinkedIn Finder

Finds contact details from LinkedIn in Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/linked-in-finder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/linked-in-finder?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/linked-in-finder?${params}`, {
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
| `url` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enrichMobile` | boolean | no |  |
| `full` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "linkedin": "https://example.com",
      "position": "string",
      "score": 1,
      "verification": {
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `linkedin` | string |  |
| `position` | string |  |
| `score` | number |  |
| `verification.status` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /linkedin` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/linked-in-finder.md) for the provider-specific parameters and requirements.

