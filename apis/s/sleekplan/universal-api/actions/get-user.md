# Sleekplan: Get User



```
GET https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes |  |

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

Through the native Sleekplan API, this operation is `GET /user/:userid` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

