# Crisp: List Connected Websites

Retrieves connected websites from Crisp.

```
GET https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-connected-websites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crisp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-connected-websites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-connected-websites?${params}`, {
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
| `pageNumber` | number | no | The page number for website paging. Default: `1`. |
| `filterConfigured` | boolean | no | Restrict to configured plugins only (1 or 0). |
| `includePlan` | boolean | no | Include the website plan subscription in the response (1 or 0). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "plan": {},
      "price": 1,
      "settings": {},
      "token": "string",
      "websiteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `plan` | object |  |
| `price` | number |  |
| `settings` | object |  |
| `token` | string |  |
| `websiteId` | string |  |

## Native endpoint

Through the native Crisp API, this operation is `GET /plugin/connect/websites/all/:page_number` (base URL `https://api.crisp.chat/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connected-websites.md) for the provider-specific parameters and requirements.

