# Process Plan: Get Tag



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-tag?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-tag?${params}`, {
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
| `tagId` | string | no | Tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tag_acc_id": "string",
      "tag_acc_level": true,
      "tag_back_color": "string",
      "tag_created_date_local": "2026-05-07T12:00:00.000Z",
      "tag_created_usr_id": "string",
      "tag_fore_color": "string",
      "tag_id": "string",
      "tag_modified_date_local": "2026-05-07T12:00:00.000Z",
      "tag_modified_usr_id": "string",
      "tag_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tag_acc_id` | string |  |
| `tag_acc_level` | boolean |  |
| `tag_back_color` | string |  |
| `tag_created_date_local` | date |  |
| `tag_created_usr_id` | string |  |
| `tag_fore_color` | string |  |
| `tag_id` | string |  |
| `tag_modified_date_local` | date |  |
| `tag_modified_usr_id` | string |  |
| `tag_name` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /tag/:tagId` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.

