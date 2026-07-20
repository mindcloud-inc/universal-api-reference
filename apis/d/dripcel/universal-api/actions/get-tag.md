# Dripcel: Get Tag

Retrieves a tag from Dripcel by ID.

```
GET https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dripcel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-tag?connectionId=$CONNECTION_ID&tagId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-tag?${params}`, {
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
| `tagId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "color": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "name": "Ava Chen",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "ok": true,
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].color` | string |  |
| `data[].createdAt` | date |  |
| `data[].description` | string |  |
| `data[].name` | string |  |
| `data[].updatedAt` | date |  |
| `ok` | boolean |  |
| `requestId` | string |  |

## Native endpoint

Through the native Dripcel API, this operation is `GET /tags/:tag_id` (base URL `https://api.dripcel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.

