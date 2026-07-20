# Damstra Forms: Update Action

Updates an action in Damstra Forms.

```
PUT https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/update-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/update-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1",
  "submitterUserId": "string",
  "lockVersion": 1,
  "fields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/update-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1",
    "submitterUserId": "string",
    "lockVersion": 1,
    "fields[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The unique identifier of the action. Example: `1`. |
| `submitterUserId` | string | yes | User identifier for the person submitting the update. |
| `lockVersion` | number | yes | Current lock version for optimistic concurrency control. |
| `fields[]` | array<object> | yes | Field values to update, using Damstra field_reference values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "href": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `href` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `PATCH /actions/{id}` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-action.md) for the provider-specific parameters and requirements.

