# Alpha TransForm: Execute On Submit Events

Executes on-submit events for a form instance in Alpha TransForm.

```
PUT https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/execute-on-submit-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/execute-on-submit-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/execute-on-submit-events', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `forminstanceid` | string | no | REQUIRED - The form instance id of the form for which you want to fire onSubmit events. |
| `actionId` | string | no | The id(s) of the action you want to fire. Blank for all actions. Can be a comma delimited list of action ids. Action Id's can be found in the onSubmit events JSON definition. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requiredVariables": [
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
| `requiredVariables` | array<object> | An array listing one or more required variables that were missing from the request if the request fails. |

## Native endpoint

Through the native Alpha TransForm API, this operation is `POST /ExecuteOnSubmitEvents` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-on-submit-events.md) for the provider-specific parameters and requirements.

