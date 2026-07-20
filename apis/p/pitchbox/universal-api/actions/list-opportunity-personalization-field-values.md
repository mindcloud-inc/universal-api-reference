# Pitchbox: List Opportunity Personalization Field Values



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunity-personalization-field-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunity-personalization-field-values?connectionId=$CONNECTION_ID&opportunityId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "opportunityId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunity-personalization-field-values?${params}`, {
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
      "id": 1,
      "personalizationField": {
        "id": 1,
        "token": "string"
      },
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `personalizationField.id` | number |  |
| `personalizationField.token` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/opportunities/:opportunityId/personalization` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-opportunity-personalization-field-values.md) for the provider-specific parameters and requirements.

