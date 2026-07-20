# AI21 Labs: Retrieve Maestro Run

Retrieves a Maestro run by ID from AI21 Labs.

```
GET https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/retrieve-maestro-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AI21 Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/retrieve-maestro-run?connectionId=$CONNECTION_ID&run_id=Paste%20the%20Maestro%20run%20id%20returned%20by%20a%20create%20action." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "run_id": "Paste the Maestro run id returned by a create action."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/retrieve-maestro-run?${params}`, {
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
| `run_id` | string | yes | The AI21 Maestro run id to retrieve. Example: `Paste the Maestro run id returned by a create action.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data_sources": [
        {}
      ],
      "error": {},
      "id": "string",
      "requirements_result": {},
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data_sources` | array<object> | Data sources used by the run when AI21 provides them. |
| `error` | object | Error details when the run fails. |
| `id` | string | The AI21 Maestro run id. |
| `requirements_result` | object | Structured requirement-evaluation output when the prompt asks for it. |
| `result` | string | The final generated output when the run completes. |
| `status` | string | The current lifecycle status of the run. |

## Native endpoint

Through the native AI21 Labs API, this operation is `GET /maestro/runs/:run_id` (base URL `https://api.ai21.com/studio/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-maestro-run.md) for the provider-specific parameters and requirements.

