# Toofr: Find Prospects

Finds prospects in Toofr by title or company.

```
GET https://connect.mindcloud.co/v1/universal/toofr/latest/actions/find-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/find-prospects?connectionId=$CONNECTION_ID&companyName=Ava%20Chen&count=1&title=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyName": "Ava Chen",
  "count": "1",
  "title": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toofr/latest/actions/find-prospects?${params}`, {
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
| `companyName` | string | yes | Company name to search prospects for. |
| `count` | number | yes | Number of prospects to return. |
| `title` | string | yes | Prospect job title to search for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Optional provider page number. |
| `tld` | string | no | Optional company top-level domain filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "confidence": 1,
      "email_address": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `confidence` | number |  |
| `email_address` | string |  |
| `first_name` | string |  |
| `last_name` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Toofr API, this operation is `GET /prospect` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-prospects.md) for the provider-specific parameters and requirements.

