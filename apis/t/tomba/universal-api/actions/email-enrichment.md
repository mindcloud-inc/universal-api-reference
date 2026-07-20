# Tomba: Email Enrichment

Retrieves contact enrichment data from Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-enrichment?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-enrichment?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enrichMobile` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "disposable": true,
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "position": "string",
      "verification": {
        "status": "string"
      },
      "webmail": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `disposable` | boolean |  |
| `email` | string |  |
| `full_name` | string |  |
| `position` | string |  |
| `verification.status` | string |  |
| `webmail` | boolean |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /enrich` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-enrichment.md) for the provider-specific parameters and requirements.

