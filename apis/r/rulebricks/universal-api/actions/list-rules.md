# Rulebricks: List Rules

Retrieves rules from Rulebricks.

```
GET https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/list-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rulebricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/list-rules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/list-rules?${params}`, {
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
| `folder` | string | no | Filter rules by folder name or folder ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "published": true,
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Rule description |
| `id` | string | Rule ID |
| `metadata` | object | Rule metadata object |
| `name` | string | Rule name |
| `published` | boolean | Whether the rule is published |
| `slug` | string | Rule slug |

## Native endpoint

Through the native Rulebricks API, this operation is `GET /admin/rules/list` (base URL `https://rulebricks.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rules.md) for the provider-specific parameters and requirements.

