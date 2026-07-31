# Excuser: Fetch Random Excuses



```
GET https://connect.mindcloud.co/v1/universal/excuser/latest/actions/fetch-random-excuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Excuser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/excuser/latest/actions/fetch-random-excuses?connectionId=$CONNECTION_ID&count=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "count": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/excuser/latest/actions/fetch-random-excuses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `count` | number | yes | Number of random excuses to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "category": "string",
          "excuse": "string",
          "id": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | array<object> | Excuse records. |
| `[].category` | string | Excuse category. |
| `[].excuse` | string | Excuse text. |
| `[].id` | number | Excuse identifier. |

## Native endpoint

Through the native Excuser API, this operation is `GET /v1/excuse/:count` (base URL `https://excuser-three.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-random-excuses.md) for the provider-specific parameters and requirements.

