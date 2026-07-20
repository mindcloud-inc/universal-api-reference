# GIRITON: List Project Categories

Retrieves all project categories from GIRITON.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-project-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-project-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-project-categories?${params}`, {
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
      "count": 1,
      "entries": [
        {}
      ],
      "newestTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of project category entries returned. |
| `entries` | array<object> | Project category entries returned by GIRITON. |
| `newestTimestamp` | date | Newest timestamp reported by GIRITON for the category list. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /projects/categories` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-categories.md) for the provider-specific parameters and requirements.

