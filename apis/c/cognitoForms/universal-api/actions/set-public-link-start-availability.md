# Cognito Forms: Set Public Link Start Availability



```
PUT https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/set-public-link-start-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cognito Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/set-public-link-start-availability" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "start": "2026-01-01T00:00:00Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/set-public-link-start-availability', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "start": "2026-01-01T00:00:00Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The Form ID |
| `start` | date | yes | Availability start date Example: `2026-01-01T00:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availabilityEnd": "2026-05-07T12:00:00.000Z",
      "availabilityStart": "2026-05-07T12:00:00.000Z",
      "notAvailableMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availabilityEnd` | date | Form availability end |
| `availabilityStart` | date | Form availability start |
| `notAvailableMessage` | string | Not available message |

## Native endpoint

Through the native Cognito Forms API, this operation is `POST /forms/:formId/public-link-availability` (base URL `https://www.cognitoforms.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-public-link-start-availability.md) for the provider-specific parameters and requirements.

