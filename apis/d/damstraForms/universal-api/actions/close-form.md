# Damstra Forms: Close Form

Closes a form in Damstra Forms.

```
PUT https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/close-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/close-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "submitterUserId": "string",
  "lockVersion": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/close-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "submitterUserId": "string",
    "lockVersion": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Path parameter id. |
| `submitterUserId` | string | yes | User identifier for the person closing the form. |
| `lockVersion` | number | yes | Current lock version for optimistic concurrency control. |

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

Through the native Damstra Forms API, this operation is `PATCH /forms/{id}` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/close-form.md) for the provider-specific parameters and requirements.

