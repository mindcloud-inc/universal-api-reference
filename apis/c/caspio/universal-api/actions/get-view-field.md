# Caspio: Get View Field

Retrieves a view field from Caspio.

```
GET https://connect.mindcloud.co/v1/universal/caspio/latest/actions/get-view-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/get-view-field?connectionId=$CONNECTION_ID&viewName=Ava%20Chen&fieldName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewName": "Ava Chen",
  "fieldName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caspio/latest/actions/get-view-field?${params}`, {
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
| `viewName` | string | yes | Target view name. |
| `fieldName` | string | yes | Target field name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | object |  |

## Native endpoint

Through the native Caspio API, this operation is `GET /v3/views/{viewName}/fields/{fieldName}` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-view-field.md) for the provider-specific parameters and requirements.

