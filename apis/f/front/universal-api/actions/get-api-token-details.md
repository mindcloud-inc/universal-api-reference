# Front: Get API Token Details

Retrieves API token details from Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/get-api-token-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/get-api-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/get-api-token-details?${params}`, {
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
      "id": [
        "string"
      ],
      "links": [
        {
          "self": [
            "https://example.com"
          ]
        }
      ],
      "name": [
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
| `id[]` | string |  |
| `links[].self[]` | string |  |
| `name[]` | string |  |

## Native endpoint

Through the native Front API, this operation is `GET /me` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-token-details.md) for the provider-specific parameters and requirements.

