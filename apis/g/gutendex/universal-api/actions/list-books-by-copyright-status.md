# Gutendex: List Books By Copyright Status

Finds books in Gutendex by copyright status.

```
GET https://connect.mindcloud.co/v1/universal/gutendex/latest/actions/list-books-by-copyright-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gutendex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gutendex/latest/actions/list-books-by-copyright-status?connectionId=$CONNECTION_ID&copyright=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "copyright": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gutendex/latest/actions/list-books-by-copyright-status?${params}`, {
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
| `copyright` | string | yes | Comma-separated values from true, false, or null. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
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
| `count` | number |  |
| `next` | string |  |
| `previous` | string |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Gutendex API, this operation is `GET /books/` (base URL `https://gutendex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-books-by-copyright-status.md) for the provider-specific parameters and requirements.

