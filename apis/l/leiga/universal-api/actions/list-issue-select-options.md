# Leiga: List Issue Select Options

Retrieves selectable issue field options from Leiga.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-issue-select-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-issue-select-options?connectionId=$CONNECTION_ID&customFiledIds%5B%5D=1&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customFiledIds[]": "1",
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-issue-select-options?${params}`, {
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
| `customFiledIds[]` | array<number> | yes | Custom Field IDs |
| `projectId` | number | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFieldId": 1,
      "filterOptionVOList": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFieldId` | number | Custom field ID. |
| `filterOptionVOList` | array<object> | Selectable options. |

## Native endpoint

Through the native Leiga API, this operation is `POST /issue/select-options` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-issue-select-options.md) for the provider-specific parameters and requirements.

