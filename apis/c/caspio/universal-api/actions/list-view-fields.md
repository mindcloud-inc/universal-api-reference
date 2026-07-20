# Caspio: List View Fields

Retrieves all view fields from Caspio.

```
GET https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-view-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-view-fields?connectionId=$CONNECTION_ID&viewName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-view-fields?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": [
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
| `Result` | array<object> |  |

## Native endpoint

Through the native Caspio API, this operation is `GET /v3/views/{viewName}/fields` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-view-fields.md) for the provider-specific parameters and requirements.

