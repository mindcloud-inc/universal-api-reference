# ZeroBounce: Domain Search

Finds company email patterns in ZeroBounce by domain.

```
GET https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/domain-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZeroBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/domain-search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/domain-search?${params}`, {
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
| `domain` | string | no |  |
| `companyName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "confidence": "string",
      "didYouMean": "string",
      "domain": "string",
      "failureReason": "string",
      "format": "string",
      "otherDomainFormats": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `confidence` | string |  |
| `didYouMean` | string |  |
| `domain` | string |  |
| `failureReason` | string |  |
| `format` | string |  |
| `otherDomainFormats` | array<object> |  |

## Native endpoint

Through the native ZeroBounce API, this operation is `GET /v2/guessformat` (base URL `https://api.zerobounce.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/domain-search.md) for the provider-specific parameters and requirements.

