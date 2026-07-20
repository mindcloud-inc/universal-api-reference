# Recommand: Get Playground

Retrieves the current playground from Recommand.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-playground
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-playground?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-playground?${params}`, {
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
      "playground": {
        "createdAt": "string",
        "id": "string",
        "isPlayground": true,
        "name": "Ava Chen",
        "teamDescription": "string",
        "updatedAt": "string",
        "useTestNetwork": true
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `playground` | object |  |
| `playground.createdAt` | string |  |
| `playground.id` | string |  |
| `playground.isPlayground` | boolean |  |
| `playground.name` | string |  |
| `playground.teamDescription` | string |  |
| `playground.updatedAt` | string |  |
| `playground.useTestNetwork` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `GET /api/v1/playgrounds/current` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-playground.md) for the provider-specific parameters and requirements.

