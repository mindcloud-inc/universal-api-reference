# Anvil: Update Organization

Updates an existing organization in Anvil.

```
PUT https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.organizationEid` | string | no | Provide Organization EID for Update Organization. |
| `variables.organizationSlug` | string | no | Provide Organization Slug for Update Organization. |
| `variables.name` | string | no | Provide Name for Update Organization. |
| `variables.logo` | file | no | Provide Logo for Update Organization. |
| `variables.billingEmail` | string | no | Provide Billing Email for Update Organization. |
| `variables.supportEmail` | string | no | Provide Support Email for Update Organization. |
| `variables.slug` | string | no | Provide Slug for Update Organization. |
| `variables.defaultSourceId` | string | no | Provide Default Source ID for Update Organization. |
| `variables.signatureProvider` | string | no | Provide Signature Provider for Update Organization. |
| `variables.config` | object | no | Provide Config for Update Organization. |
| `variables.weldCompleteEmailRecipients` | object | no | Provide Weld Complete Email Recipients for Update Organization. |
| `variables.signerViewEmailRecipients` | object | no | Provide Signer View Email Recipients for Update Organization. |
| `variables.signerCompleteEmailRecipients` | object | no | Provide Signer Complete Email Recipients for Update Organization. |
| `variables.etchCompleteEmailRecipients` | object | no | Provide Etch Complete Email Recipients for Update Organization. |
| `variables.weldCompleteEmailEnableForTest` | boolean | no | Provide Weld Complete Email Enable For Test for Update Organization. |
| `variables.stylesheetURL` | string | no | Provide Stylesheet URL for Update Organization. |
| `variables.signerOptions` | object | no | Provide Signer Options for Update Organization. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization.md) for the provider-specific parameters and requirements.

