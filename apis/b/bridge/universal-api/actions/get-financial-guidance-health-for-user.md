# Bridge: Get Financial Guidance Health for User

Retrieves financial guidance for a user in Bridge.

```
GET https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-financial-guidance-health-for-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-financial-guidance-health-for-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-financial-guidance-health-for-user?${params}`, {
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
      "domains": {
        "displayed": [
          "string"
        ],
        "recommended": [
          "string"
        ]
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domains` | object |  |
| `domains.displayed` | array<string> | List of domains displayed to the user |
| `domains.recommended` | array<string> | List of domains recommended for the user |
| `message` | string | The guidance message with analysis, context, and recommendations |

## Native endpoint

Through the native Bridge API, this operation is `GET /guidance/health/:user_uuid` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-financial-guidance-health-for-user.md) for the provider-specific parameters and requirements.

