# Sleekplan: List Satisfaction Responses



```
GET https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-satisfaction-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-satisfaction-responses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-satisfaction-responses?${params}`, {
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
| `dateEnd` | date | no |  |
| `dateStart` | date | no |  |
| `key` | string | no |  |
| `segment` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "dataRecord": "string",
      "satisfactionId": 1,
      "updated": "2026-05-07T12:00:00.000Z",
      "vote": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `dataRecord` | string |  |
| `satisfactionId` | number |  |
| `updated` | date |  |
| `vote` | number |  |

## Native endpoint

Through the native Sleekplan API, this operation is `GET /satisfaction` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-satisfaction-responses.md) for the provider-specific parameters and requirements.

