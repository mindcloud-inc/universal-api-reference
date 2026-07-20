# Flokzu: List Assignees



```
GET https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/list-assignees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flokzu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/list-assignees?connectionId=$CONNECTION_ID&assignees=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assignees": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/list-assignees?${params}`, {
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
| `assignees` | string | yes | JSON array string of email addresses and/or role names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | string | Resolved assignee entry returned by the Flokzu assignee list endpoint. |

## Native endpoint

Through the native Flokzu API, this operation is `GET /commons/assignee/list` (base URL `https://app.flokzu.com/flokzuopenapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assignees.md) for the provider-specific parameters and requirements.

