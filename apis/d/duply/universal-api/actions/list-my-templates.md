# Duply: List My Templates

Retrieves your saved templates from Duply.

```
GET https://connect.mindcloud.co/v1/universal/duply/latest/actions/list-my-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Duply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/duply/latest/actions/list-my-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/duply/latest/actions/list-my-templates?${params}`, {
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
      "contentJson": {
        "containerBackground": "string",
        "containerHeight": 1,
        "containerName": "Ava Chen",
        "containerWidth": 1
      },
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "variantName": [
        "Ava Chen"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentJson.containerBackground` | string |  |
| `contentJson.containerHeight` | number |  |
| `contentJson.containerName` | string |  |
| `contentJson.containerWidth` | number |  |
| `created` | date |  |
| `id` | string |  |
| `updated` | date |  |
| `variantName[]` | string |  |

## Native endpoint

Through the native Duply API, this operation is `GET /template` (base URL `https://gen.duply.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-my-templates.md) for the provider-specific parameters and requirements.

