# CrowdPower: Get Tag

Retrieves a tag from CrowdPower.

```
GET https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-tag?connectionId=$CONNECTION_ID&tagId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-tag?${params}`, {
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
| `tagId` | string | yes | Tag identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created_at": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created_at` | number |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native CrowdPower API, this operation is `GET tags/:tag_id` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.

