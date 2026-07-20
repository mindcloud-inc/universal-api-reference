# Florm: List Form Answers

Retrieves answers for a Florm form.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-form-answers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-form-answers?connectionId=$CONNECTION_ID&formGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-form-answers?${params}`, {
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
| `formGuid` | string | yes | GUID of the Florm form. |
| `skip` | number | no | Number of answers to skip. Default: `0`. |
| `limit` | number | no | Maximum number of answers to return. Default: `20`. |
| `searchQuery` | string | no | Search text applied to Florm answers. |
| `isCompleted` | boolean | no | Filter answers by completion state. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "guid": "string",
      "limit": 1,
      "skip": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> | List of form answers. |
| `guid` | string | GUID of the Florm form. |
| `limit` | number | Applied limit value. |
| `skip` | number | Applied skip value. |
| `total` | number | Total number of matching answers. |

## Native endpoint

Through the native Florm API, this operation is `GET /v1/answers/form/:form_guid` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-answers.md) for the provider-specific parameters and requirements.

