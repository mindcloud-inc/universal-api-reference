# ContactOut: Enrich Domain

Retrieves company details for domain names in ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-domain?connectionId=$CONNECTION_ID&domains=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domains": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-domain?${params}`, {
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
| `domains` | string | yes | An array of company domains to enrich. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": "string",
      "message": "string",
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies` | string |  |
| `message` | string |  |
| `status_code` | number |  |

## Native endpoint

Through the native ContactOut API, this operation is `POST /v1/domain/enrich` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-domain.md) for the provider-specific parameters and requirements.

