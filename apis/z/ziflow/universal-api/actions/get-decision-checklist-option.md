# Ziflow: Get Decision Checklist Option

Retrieves a decision checklist option from Ziflow.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-decision-checklist-option
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-decision-checklist-option?connectionId=$CONNECTION_ID&optionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "optionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-decision-checklist-option?${params}`, {
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
| `optionId` | string | yes | Option ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "order": 1,
      "text_field_available": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `label` | string |  |
| `order` | number |  |
| `text_field_available` | boolean |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /decision-checklist/options/:optionId` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-decision-checklist-option.md) for the provider-specific parameters and requirements.

