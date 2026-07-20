# Société.com: Check Company Exists

Checks whether a company exists in Société.com.

```
GET https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/check-company-exists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Société.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/check-company-exists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/check-company-exists?${params}`, {
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
| `numid` | string | no | Company identifier accepted by Société.com (SIREN, SIRET, VAT, or Société.com company id). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exists": true,
      "siren": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exists` | boolean | Whether the requested company identifier resolves to a known company. |
| `siren` | string | Company identifier returned or checked by the existence lookup. |
| `status` | string | Company existence or activity status. |

## Native endpoint

Through the native Société.com API, this operation is `GET /entreprise/:numid/exist` (base URL `https://api.societe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-company-exists.md) for the provider-specific parameters and requirements.

