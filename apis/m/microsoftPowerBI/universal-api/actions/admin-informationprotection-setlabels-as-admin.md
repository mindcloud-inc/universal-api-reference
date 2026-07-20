# Microsoft Power BI: InformationProtection SetLabelsAsAdmin



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-informationprotection-setlabels-as-admin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-informationprotection-setlabels-as-admin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "artifacts": {},
  "labelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-informationprotection-setlabels-as-admin', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "artifacts": {},
    "labelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `artifacts` | object | yes | A composite of Power BI item IDs for each item type |
| `labelId` | string | yes | The label ID, which must be in the user's label policy. |
| `assignmentMethod` | object | no | Specifies whether the assigned label was set by an automated process or manually. |
| `delegatedUser` | object | no | Delegated user details. A delegated user is a user within an organization whose admin sets a label on behalf of the user. Although the admin sets the label, the delegated user is marked as the label issuer. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST admin/informationprotection/setLabels` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-informationprotection-setlabels-as-admin.md) for the provider-specific parameters and requirements.

