# Tomba: Combined Enrichment

Retrieves combined enrichment data from Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/combined-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/combined-enrichment?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/combined-enrichment?${params}`, {
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
      "company": {
        "description": "string",
        "domain": "string",
        "linkedin": {
          "handle": "https://example.com"
        },
        "metrics": {
          "employees": "string"
        },
        "name": "Ava Chen"
      },
      "person": {
        "email": "ava@example.com",
        "employment": {
          "name": "Ava Chen",
          "title": "string"
        },
        "linkedin": {
          "handle": "https://example.com"
        },
        "name": {
          "fullName": "Ava Chen"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.description` | string |  |
| `company.domain` | string |  |
| `company.linkedin.handle` | string |  |
| `company.metrics.employees` | string |  |
| `company.name` | string |  |
| `person.email` | string |  |
| `person.employment.name` | string |  |
| `person.employment.title` | string |  |
| `person.linkedin.handle` | string |  |
| `person.name.fullName` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /combined/find` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/combined-enrichment.md) for the provider-specific parameters and requirements.

