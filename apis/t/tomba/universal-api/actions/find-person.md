# Tomba: Find Person

Retrieves person enrichment data from Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/find-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/find-person?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/find-person?${params}`, {
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
| `email` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "employment": {
        "domain": "string",
        "name": "Ava Chen",
        "title": "string"
      },
      "geo": {
        "countryCode": "string"
      },
      "indexedAt": "2026-05-07T12:00:00.000Z",
      "linkedin": {
        "handle": "https://example.com"
      },
      "location": "string",
      "name": {
        "fullName": "Ava Chen"
      },
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
| `email` | string |  |
| `employment.domain` | string |  |
| `employment.name` | string |  |
| `employment.title` | string |  |
| `geo.countryCode` | string |  |
| `indexedAt` | date |  |
| `linkedin.handle` | string |  |
| `location` | string |  |
| `name.fullName` | string |  |
| `verification.status` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /people/find` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-person.md) for the provider-specific parameters and requirements.

