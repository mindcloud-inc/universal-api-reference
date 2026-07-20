# Whisky Hunter: List Distilleries

Retrieves distillery details from Whisky Hunter.

```
GET https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/list-distilleries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whisky Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/list-distilleries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/list-distilleries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | Distillery country. |
| `name` | string | Distillery name. |
| `slug` | string | Distillery slug used by Whisky Hunter. |

## Native endpoint

Through the native Whisky Hunter API, this operation is `GET /distilleries_info/` (base URL `https://whiskyhunter.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-distilleries.md) for the provider-specific parameters and requirements.

