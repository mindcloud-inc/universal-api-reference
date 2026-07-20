# Sakari SMS: Get Link by ID

Retrieves a link from Sakari SMS.

```
GET https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-link-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-link-by-id?connectionId=$CONNECTION_ID&linkId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-link-by-id?${params}`, {
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
| `linkId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactTracking": true,
      "created": {
        "at": "2026-05-07T12:00:00.000Z",
        "by": {
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "name": "Ava Chen",
          "source": "string",
          "subSource": "string"
        }
      },
      "destinationUrl": "https://example.com",
      "domain": {
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "keyId": "string",
      "name": "Ava Chen",
      "shortenedUrl": "https://example.com",
      "sourceTracking": true,
      "stats": {
        "ctr": 1,
        "totalClicks": 1,
        "uniqueClicks": 1
      },
      "updated": {
        "at": "2026-05-07T12:00:00.000Z",
        "by": {
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "name": "Ava Chen",
          "source": "string",
          "subSource": "string"
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
| `contactTracking` | boolean |  |
| `created` | object |  |
| `created.at` | date |  |
| `created.by` | object |  |
| `created.by.email` | string |  |
| `created.by.firstName` | string |  |
| `created.by.id` | string |  |
| `created.by.lastName` | string |  |
| `created.by.name` | string |  |
| `created.by.source` | string |  |
| `created.by.subSource` | string |  |
| `destinationUrl` | string |  |
| `domain` | object |  |
| `domain.id` | string |  |
| `domain.name` | string |  |
| `id` | string |  |
| `keyId` | string |  |
| `name` | string |  |
| `shortenedUrl` | string |  |
| `sourceTracking` | boolean |  |
| `stats` | object |  |
| `stats.ctr` | number |  |
| `stats.totalClicks` | number |  |
| `stats.uniqueClicks` | number |  |
| `updated` | object |  |
| `updated.at` | date |  |
| `updated.by` | object |  |
| `updated.by.email` | string |  |
| `updated.by.firstName` | string |  |
| `updated.by.id` | string |  |
| `updated.by.lastName` | string |  |
| `updated.by.name` | string |  |
| `updated.by.source` | string |  |
| `updated.by.subSource` | string |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `GET /v1/accounts/:accountId/links/:linkId` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-by-id.md) for the provider-specific parameters and requirements.

