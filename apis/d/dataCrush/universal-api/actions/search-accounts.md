# DataCrush: Search Accounts

Finds accounts in DataCrush by name.

```
GET https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/search-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataCrush `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/search-accounts?connectionId=$CONNECTION_ID&name=Acme%20Corp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Acme Corp"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/search-accounts?${params}`, {
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
| `name` | string | yes | Search accounts by name. Example: `Acme Corp`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "rows": [
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
| `result` | string |  |
| `rows` | array<object> |  |

## Native endpoint

Through the native DataCrush API, this operation is `POST /account/search` (base URL `https://api.datacrush.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-accounts.md) for the provider-specific parameters and requirements.

