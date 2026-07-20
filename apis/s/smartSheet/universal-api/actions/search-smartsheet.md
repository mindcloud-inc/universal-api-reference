# Smartsheet: Search Smartsheet

Finds matching items in Smartsheet by query.

```
GET https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/search-smartsheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/search-smartsheet?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/search-smartsheet?${params}`, {
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
| `query` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scopes` | string | no |  |
| `modifiedSince` | date | no |  |
| `include` | string | no |  |
| `location` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "objectId": 1,
          "objectType": "string",
          "text": "string"
        }
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].objectId` | number |  |
| `results[].objectType` | string |  |
| `results[].text` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `GET /search` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-smartsheet.md) for the provider-specific parameters and requirements.

