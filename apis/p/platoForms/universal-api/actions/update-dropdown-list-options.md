# PlatoForms: Update Dropdown List Options

Updates dropdown list options for a form in PlatoForms.

```
PUT https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/update-dropdown-list-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/update-dropdown-list-options" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form_identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/update-dropdown-list-options', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form_identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form_identifier` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PlatoForms API returns.

## Native endpoint

Through the native PlatoForms API, this operation is `POST /form/{{form_identifier}}/field/dropdown/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dropdown-list-options.md) for the provider-specific parameters and requirements.

