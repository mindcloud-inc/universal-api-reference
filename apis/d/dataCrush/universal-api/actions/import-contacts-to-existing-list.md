# DataCrush: Search Accounts By Domain

Finds accounts in DataCrush by domain.

```
GET https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/import-contacts-to-existing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataCrush `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/import-contacts-to-existing-list?connectionId=$CONNECTION_ID&domain=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/import-contacts-to-existing-list?${params}`, {
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
| `domain` | string | yes | Domain to search for. Example: `example.com`. |

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

Through the native DataCrush API, this operation is `POST /account/search` (base URL `https://api.datacrush.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contacts-to-existing-list.md) for the provider-specific parameters and requirements.

