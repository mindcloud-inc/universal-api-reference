# Ubiqod by Skiply: Delete Codes From PIN Code List



```
DELETE https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/delete-codes-from-pin-code-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubiqod by Skiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/delete-codes-from-pin-code-list?connectionId=$CONNECTION_ID&pinCodeListId=string&codes%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pinCodeListId": "string",
  "codes[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/delete-codes-from-pin-code-list?${params}`, {
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
| `pinCodeListId` | string | yes | PIN code list ID. |
| `codes[]` | array<string> | yes | PIN codes to delete from the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "list": [
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
| `id` | string | PIN code list ID. |
| `label` | string | PIN code list label. |
| `list` | array<object> | Remaining PIN codes in the list. |

## Native endpoint

Through the native Ubiqod by Skiply API, this operation is `DELETE /pincodes/:pinCodeListId/codes` (base URL `https://api.ubiqod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-codes-from-pin-code-list.md) for the provider-specific parameters and requirements.

