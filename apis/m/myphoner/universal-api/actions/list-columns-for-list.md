# Myphoner: List Columns for List

Retrieves column information for a list in Myphoner.

```
GET https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/list-columns-for-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Myphoner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/list-columns-for-list?connectionId=$CONNECTION_ID&listId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/list-columns-for-list?${params}`, {
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
| `listId` | number | yes | The Myphoner list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "inputType": "string",
      "key": "string",
      "label": "string",
      "required": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `inputType` | string |  |
| `key` | string |  |
| `label` | string |  |
| `required` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Myphoner API, this operation is `GET /lists/:listId/columns` (base URL `https://{{credentials.subdomain}}.myphoner.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-columns-for-list.md) for the provider-specific parameters and requirements.

