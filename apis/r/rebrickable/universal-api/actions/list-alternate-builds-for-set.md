# Rebrickable: List Alternate Builds for Set

Retrieves alternate builds for a LEGO set in Rebrickable.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-alternate-builds-for-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-alternate-builds-for-set?connectionId=$CONNECTION_ID&limit=25&offset=0&setNum=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "setNum": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-alternate-builds-for-set?${params}`, {
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
| `setNum` | string | yes | Rebrickable set number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "designer_name": "Ava Chen",
      "designer_url": "https://example.com",
      "moc_img_url": "https://example.com",
      "moc_url": "https://example.com",
      "name": "Ava Chen",
      "num_parts": 1,
      "set_num": "string",
      "theme_id": 1,
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `designer_name` | string |  |
| `designer_url` | string |  |
| `moc_img_url` | string |  |
| `moc_url` | string |  |
| `name` | string |  |
| `num_parts` | number |  |
| `set_num` | string |  |
| `theme_id` | number |  |
| `year` | number |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /lego/sets/:set_num/alternates/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-alternate-builds-for-set.md) for the provider-specific parameters and requirements.

