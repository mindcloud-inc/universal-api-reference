# Global Patron: Update Form Dynamic Droplist Settings

Updates form dynamic droplist settings in Global Patron.

```
PUT https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/update-form-dynamic-droplist-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/update-form-dynamic-droplist-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/update-form-dynamic-droplist-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | ID of the form to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionSuccessful": true,
      "error": "string",
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionSuccessful` | boolean | Whether GlobalPatron reports the update was successful. |
| `error` | string | Provider error message when present. |
| `id` | string | Provider response identifier, when returned. |
| `message` | string | Provider status message. |

## Native endpoint

Through the native Global Patron API, this operation is `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=dynamicdatafieldsettings` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-dynamic-droplist-settings.md) for the provider-specific parameters and requirements.

