# Merit: List Items



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-items?${params}`, {
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
| `Code` | string | no | Broad-match item code filter from Merit docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": "string",
      "ItemId": "string",
      "Name": "Ava Chen",
      "SalesPrice": 1,
      "Type": "string",
      "Usage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string |  |
| `ItemId` | string |  |
| `Name` | string |  |
| `SalesPrice` | number |  |
| `Type` | string |  |
| `Usage` | string |  |

## Native endpoint

Through the native Merit API, this operation is `POST v1/getitems` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

