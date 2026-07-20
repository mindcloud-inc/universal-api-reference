# Kaiten: Add Tag

Creates a tag in Kaiten.

```
POST https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/add-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/add-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/add-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The tag name. |
| `color` | number | no | The numeric Kaiten tag color. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "color": 1,
      "company_id": 1,
      "created": "string",
      "id": 1,
      "name": "Ava Chen",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `color` | number |  |
| `company_id` | number |  |
| `created` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Kaiten API, this operation is `POST /tags` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tag.md) for the provider-specific parameters and requirements.

