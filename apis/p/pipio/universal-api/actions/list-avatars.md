# Pipio: List Avatars

Finds available digital avatars in Pipio.

```
GET https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-avatars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-avatars?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-avatars?${params}`, {
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
| `gender` | list | no | Filter avatars by gender. One of: `female`, `male`. |
| `ages` | list | no | Filter avatars by age band. One of: `middle`, `old`, `young`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ethnicities` | list | no | Filter avatars by ethnicity. One of: `Asian`, `Black`, `Latino / Hispanic`, `Middle Eastern`, `South Asian / Indian`, `Southeast Asian / Pacific Island`, `White / Caucasian`. |
| `shots` | list | no | Filter avatars by shot type. One of: `closeup`, `medium`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "more": true,
      "page": 1,
      "pageSize": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Avatar records for the current page. |
| `more` | boolean | Whether another page exists. |
| `page` | number | Current page number. |
| `pageSize` | number | Items requested per page. |
| `total` | number | Total matching avatars. |

## Native endpoint

Through the native Pipio API, this operation is `GET /actor` (base URL `https://avatar.pipio.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-avatars.md) for the provider-specific parameters and requirements.

