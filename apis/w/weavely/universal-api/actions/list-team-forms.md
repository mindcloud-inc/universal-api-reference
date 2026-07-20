# Weavely: List Team Forms

Retrieves forms from a Weavely team.

```
GET https://connect.mindcloud.co/v1/universal/weavely/latest/actions/list-team-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weavely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weavely/latest/actions/list-team-forms?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weavely/latest/actions/list-team-forms?${params}`, {
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
| `teamId` | string | yes | The unique identifier of the team. |
| `published` | boolean | no | If true, only returns forms that have a published version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | An array of form objects. |
| `totalItems` | number | The total number of forms available. |

## Native endpoint

Through the native Weavely API, this operation is `GET /teams/:teamId/forms` (base URL `https://api.weavely.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-forms.md) for the provider-specific parameters and requirements.

