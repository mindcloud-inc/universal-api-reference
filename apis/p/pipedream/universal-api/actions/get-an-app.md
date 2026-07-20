# Pipedream: Get an app

Retrieves details for an app from Pipedream.

```
GET https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-an-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-an-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-an-app?${params}`, {
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
| `appId` | string | yes | The Pipedream app identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authType": "string",
      "categories": [
        "string"
      ],
      "connect": {},
      "customFieldsJson": "string",
      "description": "string",
      "featuredWeight": 1,
      "id": "string",
      "imgSrc": "string",
      "name": "Ava Chen",
      "nameSlug": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authType` | string |  |
| `categories` | array<string> |  |
| `connect` | object |  |
| `customFieldsJson` | string |  |
| `description` | string |  |
| `featuredWeight` | number |  |
| `id` | string |  |
| `imgSrc` | string |  |
| `name` | string |  |
| `nameSlug` | string |  |

## Native endpoint

Through the native Pipedream API, this operation is `GET /apps/{app_id}` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-app.md) for the provider-specific parameters and requirements.

