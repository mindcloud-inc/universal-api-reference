# Société.com: Get Company Legal Information

Retrieves company legal information from Société.com.

```
GET https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-company-legal-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Société.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-company-legal-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-company-legal-information?${params}`, {
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
      "infolegales": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `infolegales` | object | Canonical legal information object returned for the company. |

## Native endpoint

Through the native Société.com API, this operation is `GET /entreprise/:numid/infoslegales` (base URL `https://api.societe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-legal-information.md) for the provider-specific parameters and requirements.

