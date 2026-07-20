# SurveyMethods: List Email List Contacts



```
GET https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-email-list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveyMethods `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-email-list-contacts?connectionId=$CONNECTION_ID&emailListCode=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailListCode": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-email-list-contacts?${params}`, {
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
| `emailListCode` | string | yes | SurveyMethods email list code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_field_labels": {
        "label1": "string",
        "label2": "string",
        "label3": "string",
        "label4": "string",
        "label5": "string"
      },
      "email_list": [
        {
          "custom_field_values": {
            "value1": "ava@example.com",
            "value2": "ava@example.com",
            "value3": "ava@example.com",
            "value4": "ava@example.com",
            "value5": "ava@example.com"
          },
          "email": "ava@example.com"
        }
      ],
      "list_type": "string",
      "rowcount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_field_labels` | object |  |
| `custom_field_labels.label1` | string |  |
| `custom_field_labels.label2` | string |  |
| `custom_field_labels.label3` | string |  |
| `custom_field_labels.label4` | string |  |
| `custom_field_labels.label5` | string |  |
| `email_list` | array<object> |  |
| `email_list[].custom_field_values` | object |  |
| `email_list[].custom_field_values.value1` | string |  |
| `email_list[].custom_field_values.value2` | string |  |
| `email_list[].custom_field_values.value3` | string |  |
| `email_list[].custom_field_values.value4` | string |  |
| `email_list[].custom_field_values.value5` | string |  |
| `email_list[].email` | string |  |
| `list_type` | string |  |
| `rowcount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native SurveyMethods API, this operation is `GET /:loginId/:apiKey/emaillists/:emailListCode/` (base URL `https://api.surveymethods.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-list-contacts.md) for the provider-specific parameters and requirements.

