# MerrenIO: Change Survey Category



```
PUT https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/change-survey-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MerrenIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/change-survey-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "string",
  "category": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/change-survey-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "string",
    "category": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes | Survey to update. |
| `category` | string | yes | New survey category. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MerrenIO API returns.

## Native endpoint

Through the native MerrenIO API, this operation is `POST /survey/update` (base URL `https://app.merren.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-survey-category.md) for the provider-specific parameters and requirements.

