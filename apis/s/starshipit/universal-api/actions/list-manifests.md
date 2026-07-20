# Starshipit: List Manifests



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-manifests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-manifests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-manifests?${params}`, {
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
| `page` | number | no | Page to show. Default: 1 |
| `limit` | number | no | Maximum number of records in the result. Default: 50. Maximum: 250 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "manifests": [
        {
          "carrierId": 1,
          "date": "2026-05-07T12:00:00.000Z",
          "fileName1": "Ava Chen",
          "fileName2": "Ava Chen",
          "id": 1,
          "name": "Ava Chen",
          "number": 1,
          "numberArticles": 1,
          "numberConsignments": 1
        }
      ],
      "success": true,
      "totalCount": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `manifests` | array<object> |  |
| `manifests[].carrierId` | number |  |
| `manifests[].date` | date |  |
| `manifests[].fileName1` | string |  |
| `manifests[].fileName2` | string |  |
| `manifests[].id` | number |  |
| `manifests[].name` | string |  |
| `manifests[].number` | number |  |
| `manifests[].numberArticles` | number |  |
| `manifests[].numberConsignments` | number |  |
| `success` | boolean |  |
| `totalCount` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /manifests` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-manifests.md) for the provider-specific parameters and requirements.

