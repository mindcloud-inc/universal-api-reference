# Process Plan: List Automated Action Properties for Automated Action



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-automated-action-properties-for-automated-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-automated-action-properties-for-automated-action?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-automated-action-properties-for-automated-action?${params}`, {
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
| `automatedActionId` | string | no | Automated action ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automated_action_property_list": [
        {
          "aap_field_help": "string",
          "aap_field_label": "string",
          "aap_field_option_list": [
            {
              "text": "string",
              "value": "string"
            }
          ],
          "aap_field_postback": true,
          "aap_field_required": true,
          "aap_field_type": 1,
          "aap_property_type": 1,
          "aap_value_type": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automated_action_property_list[].aap_field_help` | string |  |
| `automated_action_property_list[].aap_field_label` | string |  |
| `automated_action_property_list[].aap_field_option_list[].text` | string |  |
| `automated_action_property_list[].aap_field_option_list[].value` | string |  |
| `automated_action_property_list[].aap_field_postback` | boolean |  |
| `automated_action_property_list[].aap_field_required` | boolean |  |
| `automated_action_property_list[].aap_field_type` | number |  |
| `automated_action_property_list[].aap_property_type` | number |  |
| `automated_action_property_list[].aap_value_type` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /automated_action/:automatedActionId/automated_action_property/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-automated-action-properties-for-automated-action.md) for the provider-specific parameters and requirements.

