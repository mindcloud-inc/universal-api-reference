# Piloterr: Get Trustpilot Company Info



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-trustpilot-company-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-trustpilot-company-info?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-trustpilot-company-info?${params}`, {
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
| `query` | string | yes | Trustpilot company URL, domain, or slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "reviewCount": 1,
      "reviewScore": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `reviewCount` | number |  |
| `reviewScore` | number |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /trustpilot/company/info` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trustpilot-company-info.md) for the provider-specific parameters and requirements.

