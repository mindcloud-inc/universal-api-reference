# Lightfunnels: Retrieve Integrations



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/retrieve-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/retrieve-integrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/retrieve-integrations?${params}`, {
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
      "account": {
        "integrations": [
          {
            "id": "string",
            "type": "string",
            "url": "https://example.com"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object | Account root. |
| `account.integrations` | array<object> | Installed integrations. |
| `account.integrations[].id` | string | Integration id. |
| `account.integrations[].type` | string | Integration type. |
| `account.integrations[].url` | string | Integration url. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-integrations.md) for the provider-specific parameters and requirements.

