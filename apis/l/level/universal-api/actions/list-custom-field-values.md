# Level: List Custom Field Values

Retrieves custom field values from Level.

```
GET https://connect.mindcloud.co/v1/universal/level/latest/actions/list-custom-field-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/level/latest/actions/list-custom-field-values?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/level/latest/actions/list-custom-field-values?${params}`, {
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
| `assignedToId` | string | no | Filter to only include values assigned to the specified group or device. |
| `customFieldId` | string | no | Filter to only include values for the specified custom field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "assignedToId": "string",
          "customFieldId": "string",
          "customFieldName": "Ava Chen",
          "value": "string"
        }
      ],
      "hasMore": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].assignedToId` | string |  |
| `data[].customFieldId` | string |  |
| `data[].customFieldName` | string |  |
| `data[].value` | string |  |
| `hasMore` | boolean |  |

## Native endpoint

Through the native Level API, this operation is `GET /custom_field_values` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-custom-field-values.md) for the provider-specific parameters and requirements.

