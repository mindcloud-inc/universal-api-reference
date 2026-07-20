# Reverse Contact: Resolve Person From Email



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/resolve-person-from-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/resolve-person-from-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/resolve-person-from-email?${params}`, {
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
| `email` | string | yes | Email address to resolve. |
| `webhookUrl` | string | no | HTTPS callback URL for async results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentCompanyLinkedinId": "https://example.com",
      "currentCompanyName": "Ava Chen",
      "currentPositionTitle": "string",
      "firstName": "Ava",
      "headline": "string",
      "lastName": "Chen",
      "linkedinUrl": "https://example.com",
      "location": {
        "city": "string",
        "country": "string",
        "countryCode": "string",
        "state": "string"
      },
      "publicId": "string",
      "updateDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentCompanyLinkedinId` | string |  |
| `currentCompanyName` | string |  |
| `currentPositionTitle` | string |  |
| `firstName` | string |  |
| `headline` | string |  |
| `lastName` | string |  |
| `linkedinUrl` | string |  |
| `location.city` | string |  |
| `location.country` | string |  |
| `location.countryCode` | string |  |
| `location.state` | string |  |
| `publicId` | string |  |
| `updateDate` | date |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `POST /v2/resolve/persons/email` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-person-from-email.md) for the provider-specific parameters and requirements.

