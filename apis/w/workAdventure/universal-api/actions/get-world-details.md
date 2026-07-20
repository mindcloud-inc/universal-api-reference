# WorkAdventure: Get world details

Retrieves details for a WorkAdventure world by slug.

```
GET https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/get-world-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/get-world-details?connectionId=$CONNECTION_ID&worldSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "worldSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/get-world-details?${params}`, {
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
| `worldSlug` | string | yes | The world slug from the WorkAdventure world URL, for example `mindcloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activated": true,
      "created_at": "string",
      "is_premium": true,
      "max_user_capacity": 1,
      "name": "Ava Chen",
      "slug": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activated` | boolean |  |
| `created_at` | string |  |
| `is_premium` | boolean |  |
| `max_user_capacity` | number |  |
| `name` | string |  |
| `slug` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native WorkAdventure API, this operation is `GET /api/v1/worlds/:worldSlug` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-world-details.md) for the provider-specific parameters and requirements.

