# Kaiten: Retrieve List of Spaces

Retrieves spaces from Kaiten.

```
GET https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-spaces?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "access": "string",
      "archived": true,
      "boards": [
        {
          "id": 1,
          "title": "string"
        }
      ],
      "company_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "path": "string",
      "primary_path": true,
      "sort_order": 1,
      "title": "string",
      "uid": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `archived` | boolean |  |
| `boards[].id` | number |  |
| `boards[].title` | string |  |
| `company_id` | number |  |
| `created` | date |  |
| `id` | number |  |
| `path` | string |  |
| `primary_path` | boolean |  |
| `sort_order` | number |  |
| `title` | string |  |
| `uid` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Kaiten API, this operation is `GET /spaces` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-list-of-spaces.md) for the provider-specific parameters and requirements.

