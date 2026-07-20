# DotCMS: List Permissions

Retrieves permission metadata definitions from DotCMS.

```
GET https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DotCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-permissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-permissions?${params}`, {
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
      "entity": {
        "levels": [
          "string"
        ],
        "scopes": [
          "string"
        ]
      },
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity.levels[]` | string |  |
| `entity.scopes[]` | string |  |
| `pagination` | object |  |

## Native endpoint

Through the native DotCMS API, this operation is `GET /api/v1/permissions` (base URL `https://demo.dotcms.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-permissions.md) for the provider-specific parameters and requirements.

