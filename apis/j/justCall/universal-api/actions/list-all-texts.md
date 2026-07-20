# JustCall: List All Texts

Retrieves texts from JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-texts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-texts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-texts?${params}`, {
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
| `fromDateTime` | string | no |  |
| `toDateTime` | string | no |  |
| `lastSmsIdFetched` | number | no |  |
| `contactNumber` | string | no |  |
| `justcallNumber` | string | no |  |
| `smsDirection` | string | no |  |
| `smsContent` | string | no |  |
| `sort` | string | no |  |
| `order` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "currentPage": 1,
      "data": [
        {}
      ],
      "nextPageLink": "https://example.com",
      "perPage": 1,
      "prevPageLink": "https://example.com",
      "status": "string",
      "totalTexts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `nextPageLink` | string |  |
| `perPage` | number |  |
| `prevPageLink` | string |  |
| `status` | string |  |
| `totalTexts` | number |  |

## Native endpoint

Through the native JustCall API, this operation is `GET /v2.1/texts` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-texts.md) for the provider-specific parameters and requirements.

