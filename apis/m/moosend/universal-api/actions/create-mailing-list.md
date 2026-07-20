# Moosend: Create Mailing List

Creates a new mailing list in Moosend.

```
POST https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-mailing-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "preferences": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-mailing-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "preferences": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the email list. |
| `confirmationPage` | string | no | The URL of the page displayed at the end of the subscription process. |
| `redirectAfterUnsubscribePage` | string | no | The URL of the redirect page when users unsubscribe from your email list. |
| `preferences` | list<object> | yes | The Preferences field options. SelectType The data type of the field. Possible values can be SingleSelect or MultiSelect . Required field. Options Max options 10 IsRequired If the field is required. Default value false . |
| `preferencePageId` | string | no | The preference page id. |

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

Through the native Moosend API, this operation is `POST /lists/create.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mailing-list.md) for the provider-specific parameters and requirements.

