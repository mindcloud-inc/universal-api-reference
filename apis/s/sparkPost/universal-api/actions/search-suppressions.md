# SparkPost: Search Suppressions



```
GET https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/search-suppressions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/search-suppressions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/search-suppressions?${params}`, {
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
| `page` | number | no | Suppression search page number. |
| `perPage` | number | no | Maximum suppressions to return per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "description": "string",
      "recipient": "string",
      "source": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `description` | string |  |
| `recipient` | string |  |
| `source` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SparkPost API, this operation is `GET /suppression-list` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-suppressions.md) for the provider-specific parameters and requirements.

