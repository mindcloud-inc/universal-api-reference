# Platrum: Get article

Retrieves a knowledge article from Platrum by ID.

```
GET https://connect.mindcloud.co/v1/universal/platrum/latest/actions/get-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platrum/latest/actions/get-article?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platrum/latest/actions/get-article?${params}`, {
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
| `id` | number | yes | Article ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Platrum API, this operation is `POST /wiki/api/article/get` (base URL `https://3e8e7be.platrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article.md) for the provider-specific parameters and requirements.

