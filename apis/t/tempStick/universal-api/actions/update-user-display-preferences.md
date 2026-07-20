# Temp Stick: Update User Display Preferences

Updates Temp Stick display preferences for the current user.

```
PUT https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/update-user-display-preferences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temp Stick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/update-user-display-preferences" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timezone": "America/New_York",
  "tempPref": "F"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/update-user-display-preferences', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timezone": "America/New_York",
    "tempPref": "F"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timezone` | string | yes | Time zone of the user, functionally used in determining if an alert should trigger if a time window is set Default: `America/New_York`. |
| `tempPref` | string | yes | Display alerts in fahrenheit or celsius Default: `F`. |
| `chartFill` | number | no | Set whether to have the chart normalized on the Y-axis Default: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Temp Stick API returns.

## Native endpoint

Through the native Temp Stick API, this operation is `POST /user/display-preferences` (base URL `https://tempstickapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-display-preferences.md) for the provider-specific parameters and requirements.

