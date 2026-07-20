# Responsr: Get Default Project



```
GET https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Responsr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-project?${params}`, {
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
      "appType": "string",
      "appTypeId": 1,
      "description": "string",
      "integrationKey": "string",
      "lifeTime": "string",
      "name": "Ava Chen",
      "participants": [
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
| `appType` | string |  |
| `appTypeId` | number |  |
| `description` | string |  |
| `integrationKey` | string |  |
| `lifeTime` | string |  |
| `name` | string |  |
| `participants` | array<object> |  |

## Native endpoint

Through the native Responsr API, this operation is `GET /api/v1.0/projects/default` (base URL `https://app.responsr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-project.md) for the provider-specific parameters and requirements.

