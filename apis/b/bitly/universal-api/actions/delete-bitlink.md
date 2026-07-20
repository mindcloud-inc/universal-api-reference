# Bitly: Delete Bitlink

Deletes an unedited hash bitlink from Bitly.

```
DELETE https://connect.mindcloud.co/v1/universal/bitly/latest/actions/delete-bitlink
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/delete-bitlink?connectionId=$CONNECTION_ID&bitlink=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bitlink": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/delete-bitlink?${params}`, {
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
| `bitlink` | string | yes | The Bitly bitlink to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "linksDeleted": [
        {
          "id": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `linksDeleted[].id` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `DELETE /bitlinks/:bitlink` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bitlink.md) for the provider-specific parameters and requirements.

