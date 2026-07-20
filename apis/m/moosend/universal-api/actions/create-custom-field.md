# Moosend: Create Custom Field

Creates a new custom field in Moosend.

```
POST https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailingListId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailingListId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailingListId` | string | yes | The ID of the email list where the custom field is created. |
| `name` | string | yes | The name of the custom field. |
| `customFieldType` | string | no | Specifies the data type of the custom field. This must be one of the following values. Text (Default) - accepts any text value as input. Number - accepts only numeric values as input. DateTime - accepts only date values as input, with or without time. SingleSelectDropdown - accepts only values explicitly defined in a list. CheckBox - accepts only values of true or false. |
| `options` | string | no | If you want to create a SingleSelectDropdown custom field, you must set this parameter to specify the available options for the user to choose from. Use a comma (,) to separate different options. |
| `isRequired` | boolean | no | Specifies whether the custom field is mandatory or not when adding a subscriber to your list. You must specify a value of true or false (Default). |
| `isHidden` | boolean | no | Specifies whether the custom field is visible to your subscribers in the Update Profile page. You must specify a value of true or false (Default). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Moosend API, this operation is `POST /lists/{{MailingListID}}/customfields/create.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-field.md) for the provider-specific parameters and requirements.

