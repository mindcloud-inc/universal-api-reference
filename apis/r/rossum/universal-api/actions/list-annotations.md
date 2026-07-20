# Rossum: List Annotations

Retrieves annotations from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-annotations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-annotations?${params}`, {
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
| `queue` | string | no | Queue ID filter, comma-separated for multiple values. |
| `status` | string | no | Annotation status filter; comma-separated for multiple values. |
| `pageSize` | number | no | Number of results per page (max 100). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "next": {},
        "previous": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.next` | object |  |
| `pagination.previous` | object |  |

## Native endpoint

Through the native Rossum API, this operation is `GET /annotations` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-annotations.md) for the provider-specific parameters and requirements.

