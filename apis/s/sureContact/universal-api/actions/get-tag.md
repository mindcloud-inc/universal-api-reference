# SureContact: Get Tag

Retrieves a specific tag from SureContact.

```
GET https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/get-tag?connectionId=$CONNECTION_ID&tagUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/get-tag?${params}`, {
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
| `tagUuid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "name": "Ava Chen",
      "slug": "string",
      "usage_count": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `name` | string |  |
| `slug` | string |  |
| `usage_count` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native SureContact API, this operation is `GET api/v1/public/tags/:tag_uuid` (base URL `https://api.surecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.

