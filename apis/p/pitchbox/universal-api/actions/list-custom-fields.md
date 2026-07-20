# Pitchbox: List Custom Fields



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-custom-fields?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        "string"
      ],
      "currency": "string",
      "description": "string",
      "groupName": "Ava Chen",
      "id": 1,
      "isRequiredMilestoneChange": true,
      "isRequiredOppDetails": true,
      "isRequiredPersonalization": true,
      "label": "string",
      "name": "Ava Chen",
      "opportunityUsage": true,
      "token": "string",
      "tokenWithPrefix": "string",
      "type": "string",
      "typeIcon": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<string> |  |
| `currency` | string |  |
| `description` | string |  |
| `groupName` | string |  |
| `id` | number |  |
| `isRequiredMilestoneChange` | boolean |  |
| `isRequiredOppDetails` | boolean |  |
| `isRequiredPersonalization` | boolean |  |
| `label` | string |  |
| `name` | string |  |
| `opportunityUsage` | boolean |  |
| `token` | string |  |
| `tokenWithPrefix` | string |  |
| `type` | string |  |
| `typeIcon` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/custom_fields` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-fields.md) for the provider-specific parameters and requirements.

