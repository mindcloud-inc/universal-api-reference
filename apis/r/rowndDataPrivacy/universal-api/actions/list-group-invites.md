# Rownd Data Privacy: List Group Invites



```
GET https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/list-group-invites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/list-group-invites?connectionId=$CONNECTION_ID&group=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/list-group-invites?${params}`, {
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
| `group` | string | yes | Rownd group identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "total_results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Group invite records returned by Rownd. |
| `total_results` | number | Total number of invites returned. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `GET /groups/:group/invites` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-invites.md) for the provider-specific parameters and requirements.

