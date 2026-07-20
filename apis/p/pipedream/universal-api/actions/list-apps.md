# Pipedream: List apps

Retrieves a list of apps from Pipedream.

```
GET https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/list-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/list-apps?${params}`, {
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
| `hasActions` | string | no | Pass `1` to only return apps with public actions. |
| `hasComponents` | string | no | Pass `1` to only return apps with public triggers or actions. |
| `hasTriggers` | string | no | Pass `1` to only return apps with public triggers. |
| `query` | string | no | Optional query string to filter the list of apps. |

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

Through the native Pipedream API, this operation is `GET /apps` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-apps.md) for the provider-specific parameters and requirements.

