# Deepset: Get Permissions

Retrieves permissions for your Deepset organization.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-permissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-permissions?${params}`, {
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
      "data": [
        {
          "action": "string",
          "asset": "string"
        }
      ],
      "has_more": true,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].action` | string |  |
| `data[].asset` | string |  |
| `has_more` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v1/organization/permissions` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-permissions.md) for the provider-specific parameters and requirements.

