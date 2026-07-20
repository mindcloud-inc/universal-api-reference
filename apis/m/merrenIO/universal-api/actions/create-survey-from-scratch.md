# MerrenIO: Create Survey From Scratch



```
POST https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/create-survey-from-scratch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MerrenIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/create-survey-from-scratch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.name": "Ava Chen",
  "input.category": "string",
  "input.created_by": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/create-survey-from-scratch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.name": "Ava Chen",
    "input.category": "string",
    "input.created_by": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.name` | string | yes | Name of the new survey. |
| `input.category` | string | yes | Survey category label, such as Other or Customer Satisfaction. |
| `input.created_by` | string | yes | Creator email used by Merren when creating the survey. |
| `input.description` | string | no | Optional survey description. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MerrenIO API returns.

## Native endpoint

Through the native MerrenIO API, this operation is `POST /survey/create` (base URL `https://app.merren.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-survey-from-scratch.md) for the provider-specific parameters and requirements.

