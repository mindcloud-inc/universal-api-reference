# Pitchbox: List Opportunity Custom Field Values



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunity-custom-field-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunity-custom-field-values?connectionId=$CONNECTION_ID&opportunityId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "opportunityId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunity-custom-field-values?${params}`, {
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
| `opportunityId` | number | yes | The opportunity id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customField": {
        "id": 1,
        "name": "Ava Chen",
        "token": "string"
      },
      "id": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customField.id` | number |  |
| `customField.name` | string |  |
| `customField.token` | string |  |
| `id` | number |  |
| `value` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/opportunities/:opportunityId/custom_fields` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-opportunity-custom-field-values.md) for the provider-specific parameters and requirements.

