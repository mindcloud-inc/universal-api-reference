# Sleekplan: List Update Satisfaction Responses



```
GET https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-update-satisfaction-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-update-satisfaction-responses?connectionId=$CONNECTION_ID&limit=25&offset=0&updateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "updateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-update-satisfaction-responses?${params}`, {
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
| `segment` | string | no |  |
| `updateId` | string | yes |  |

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

Through the native Sleekplan API, this operation is `GET /update/:updateid/satisfaction` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-update-satisfaction-responses.md) for the provider-specific parameters and requirements.

