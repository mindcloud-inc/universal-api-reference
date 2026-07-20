# MailUp: List Imports

Retrieves existing import jobs from MailUp.

```
GET https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-imports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-imports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-imports?${params}`, {
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
      "filename": "Ava Chen",
      "idImport": 1,
      "idList": 1,
      "rows": 1,
      "startDate": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string |  |
| `idImport` | number |  |
| `idList` | number |  |
| `rows` | number |  |
| `startDate` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native MailUp API, this operation is `GET Console/Imports` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-imports.md) for the provider-specific parameters and requirements.

