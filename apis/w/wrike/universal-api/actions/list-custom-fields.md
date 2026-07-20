# Wrike: List Custom Fields

Finds custom fields in Wrike.

```
GET https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-custom-fields?${params}`, {
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
      "accountId": "string",
      "dataUsageStatistics": {},
      "description": "string",
      "id": "string",
      "settings": {},
      "sharedIds": [
        "string"
      ],
      "sharing": "string",
      "spaceId": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `dataUsageStatistics` | object |  |
| `description` | string |  |
| `id` | string |  |
| `settings` | object |  |
| `sharedIds` | array<string> |  |
| `sharing` | string |  |
| `spaceId` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Wrike API, this operation is `GET /customfields` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-fields.md) for the provider-specific parameters and requirements.

