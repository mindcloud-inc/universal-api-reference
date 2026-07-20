# Sleekplan: List Users



```
GET https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-users?${params}`, {
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
| `search` | string | no |  |
| `segment` | string | no |  |
| `sort` | string | no |  |
| `sortDir` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anonymous": true,
      "created": "2026-05-07T12:00:00.000Z",
      "dataFullName": "Ava Chen",
      "dataId": "string",
      "dataImg": "string",
      "dataMail": "string",
      "dataName": "Ava Chen",
      "statsComments": 1,
      "statsFeedback": 1,
      "statsVotes": 1,
      "updated": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anonymous` | boolean |  |
| `created` | date |  |
| `dataFullName` | string |  |
| `dataId` | string |  |
| `dataImg` | string |  |
| `dataMail` | string |  |
| `dataName` | string |  |
| `statsComments` | number |  |
| `statsFeedback` | number |  |
| `statsVotes` | number |  |
| `updated` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Sleekplan API, this operation is `GET /users` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

