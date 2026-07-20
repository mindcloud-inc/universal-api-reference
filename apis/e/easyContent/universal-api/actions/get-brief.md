# EasyContent: Get Brief

Retrieves a brief from EasyContent by ID.

```
GET https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/get-brief
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/get-brief?connectionId=$CONNECTION_ID&briefId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "briefId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/get-brief?${params}`, {
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
| `briefId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        1
      ],
      "id": 1,
      "name": "Ava Chen",
      "notes": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories[]` | number |  |
| `id` | number |  |
| `name` | string |  |
| `notes` | string |  |

## Native endpoint

Through the native EasyContent API, this operation is `GET /v2/content/briefs/:briefId` (base URL `https://easycontent.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-brief.md) for the provider-specific parameters and requirements.

