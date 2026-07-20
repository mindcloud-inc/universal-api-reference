# Florm: List Form Step Answers

Retrieves answers for a Florm form step.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-form-step-answers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-form-step-answers?connectionId=$CONNECTION_ID&formGuid=string&stepId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formGuid": "string",
  "stepId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/list-form-step-answers?${params}`, {
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
| `stepId` | number | yes | Numeric Florm step identifier. |
| `skip` | number | no | Number of answer records to skip. Default: `0`. |
| `limit` | number | no | Maximum number of answer records to return. Default: `30`. |
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
| `answers` | array<object> | List of step answers. |
| `limit` | number | Applied limit value. |
| `skip` | number | Applied skip value. |
| `total` | number | Total number of matching answers. |

## Native endpoint

Through the native Florm API, this operation is `GET /v1/answers/form/:form_guid/step/:step_id` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-step-answers.md) for the provider-specific parameters and requirements.

