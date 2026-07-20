# Porsline: List Survey Variables



```
GET https://connect.mindcloud.co/v1/universal/porsline/latest/actions/list-survey-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/list-survey-variables?connectionId=$CONNECTION_ID&survey_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "survey_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/porsline/latest/actions/list-survey-variables?${params}`, {
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
| `survey_id` | number | yes | The id of the target survey. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "variables": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `variables` | array | Survey variable objects returned by Porsline. |

## Native endpoint

Through the native Porsline API, this operation is `GET /api/surveys/:survey_id/variables/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-survey-variables.md) for the provider-specific parameters and requirements.

