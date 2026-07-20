# Campaign Refinery: Get Tag by Name

Retrieves a tag by name from Campaign Refinery.

```
GET https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-tag-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Refinery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-tag-by-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-tag-by-name?${params}`, {
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
| `name` | string | yes | Campaign Refinery tag name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tag_created_dts": "2026-05-07T12:00:00.000Z",
      "tag_id": 1,
      "tag_name": "Ava Chen",
      "tag_uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tag_created_dts` | date | Tag creation timestamp. |
| `tag_id` | number | Campaign Refinery numeric tag ID. |
| `tag_name` | string | Tag name. |
| `tag_uuid` | string | Campaign Refinery tag UUID. |

## Native endpoint

Through the native Campaign Refinery API, this operation is `GET /tags/get-tag` (base URL `https://app.campaignrefinery.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag-by-name.md) for the provider-specific parameters and requirements.

